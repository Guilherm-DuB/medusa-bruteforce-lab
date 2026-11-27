# Cenário 2 — Brute Force em formulário Web (DVWA)

## 1. Objetivo

Simular um teste de força bruta contra um formulário de autenticação web utilizando Kali Linux e Medusa, em um ambiente controlado.

O objetivo foi observar o funcionamento do módulo `web-form` e analisar suas limitações durante a identificação de credenciais.

## 2. Ambiente utilizado

- **Sistema atacante:** Kali Linux
- **Máquina-alvo:** Metasploitable 2
- **Aplicação:** Damn Vulnerable Web Application (DVWA)
- **Endereço IP:** `192.168.56.102`
- **Ferramenta:** Medusa 2.3-3
- **Módulo utilizado:** `web-form`
- **Nível de segurança do DVWA:** Low

## 3. Configuração do DVWA

Após acessar a aplicação, foi configurado o nível de segurança como Low.

Em seguida, foi acessada a funcionalidade **Brute Force**, que disponibiliza um formulário com os campos:

- Username
- Password

Também foi analisado o código-fonte da funcionalidade para identificar os parâmetros utilizados no processo de autenticação.

## 4. Análise da requisição HTTP

Utilizando as ferramentas de desenvolvedor do Firefox, na aba Network, foi possível observar as requisições realizadas durante as tentativas de autenticação.

Foram identificados os seguintes parâmetros:

- `username`: usuário informado.
- `password`: senha informada.
- `Login`: parâmetro de envio do formulário.

A análise também permitiu observar a resposta HTTP retornada pela aplicação.

## 5. Execução do Medusa

Foi utilizado o módulo `web-form` para realizar as tentativas automatizadas de autenticação.

O comando utilizado seguiu a seguinte estrutura:

```bash
medusa -h 192.168.56.102 -U users.txt -P pass.txt -M web-form
```

Foram adicionados parâmetros específicos para indicar o caminho do formulário, os campos enviados, a mensagem de falha e o cabeçalho de sessão.

## 6. Resultado observado

Durante a execução, o Medusa apresentou mensagens `ACCOUNT FOUND` e classificou diferentes combinações de usuário e senha como `SUCCESS`.

Entretanto, os resultados não foram considerados confiáveis, pois combinações inválidas também foram classificadas como bem-sucedidas.

Dessa forma, não foi possível confirmar a descoberta de credenciais válidas por meio da ferramenta.

## 7. Análise técnica

Durante o experimento, foi identificada uma limitação na interpretação das respostas HTTP pelo módulo `web-form`.

O módulo utiliza o parâmetro `DENY-SIGNAL` para identificar mensagens de falha. Quando o texto configurado não é encontrado na resposta recebida, a tentativa pode ser classificada como bem-sucedida.

No cenário testado, esse comportamento resultou em falsos positivos.

Isso demonstrou a importância de analisar as respostas da aplicação e validar os resultados obtidos por ferramentas automatizadas.

## 8. Medidas defensivas

Algumas medidas que ajudam a reduzir o risco de ataques de força bruta em aplicações web são:

- Implementar limites de tentativas de autenticação.
- Utilizar mecanismos de bloqueio temporário de contas.
- Adotar senhas fortes e exclusivas.
- Implementar autenticação multifator (MFA).
- Monitorar tentativas de autenticação suspeitas.
- Utilizar mecanismos de CAPTCHA quando apropriado.

## 9. Conclusão

O experimento permitiu compreender o funcionamento do módulo `web-form` do Medusa e sua utilização em testes de autenticação web.

Também foi possível identificar uma limitação na interpretação das respostas HTTP, que ocasionou resultados inconclusivos.

A atividade reforçou a importância de não considerar automaticamente os resultados de ferramentas de segurança como evidências definitivas, sendo necessária a validação das informações obtidas.

## 10. Evidências

As capturas de tela deste cenário estão organizadas no diretório:

```text
screenshots/web-dvwa/
```

As evidências incluem:

- Configuração do nível de segurança do DVWA.
- Formulário de autenticação.
- Análise da requisição HTTP.
- Execução do Medusa.
- Resultado das tentativas automatizadas.

## 11. Aviso de segurança

Este laboratório foi realizado exclusivamente em ambiente virtual controlado, com finalidade educacional.

As técnicas apresentadas devem ser utilizadas somente em sistemas próprios ou com autorização explícita.
