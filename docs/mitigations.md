# Medidas de Mitigação

## 1. Introdução

Os ataques de força bruta e Password Spraying exploram possíveis fragilidades nos mecanismos de autenticação, principalmente quando são utilizadas senhas fracas ou não existem controles adequados contra tentativas repetidas de acesso.

Este documento apresenta medidas de segurança que podem ser adotadas para reduzir os riscos identificados nos cenários do laboratório.

## 2. Proteção do serviço FTP

O serviço FTP pode estar sujeito a tentativas automatizadas de descoberta de credenciais.

**Medidas recomendadas:**

- Utilizar senhas fortes e exclusivas.
- Desabilitar contas desnecessárias.
- Restringir o acesso ao serviço por endereço IP.
- Limitar tentativas consecutivas de autenticação.
- Monitorar registros de acesso e tentativas malsucedidas.
- Preferir protocolos seguros, como SFTP ou FTPS, quando aplicável.

## 3. Proteção de aplicações web (DVWA)

Formulários de autenticação podem ser explorados por meio de tentativas automatizadas de descoberta de senhas.

**Medidas recomendadas:**

- Implementar limitação de tentativas de login.
- Adotar mecanismos de bloqueio temporário após sucessivas falhas.
- Utilizar senhas fortes.
- Implementar autenticação multifator (MFA).
- Registrar e monitorar tentativas de autenticação.
- Utilizar mecanismos de proteção contra automação abusiva.

## 4. Proteção do serviço SMB

O serviço SMB pode ser alvo de ataques de força bruta e Password Spraying, principalmente quando existem contas com senhas fracas ou configurações inadequadas.

**Medidas recomendadas:**

- Utilizar senhas fortes e políticas de autenticação.
- Desabilitar contas desnecessárias.
- Restringir o acesso às portas 139 e 445.
- Desabilitar versões antigas e inseguras do SMB.
- Monitorar tentativas de autenticação malsucedidas.
- Aplicar políticas de bloqueio de contas quando apropriado.

## 5. Monitoramento e prevenção

Além das medidas específicas para cada serviço, algumas práticas contribuem para a segurança geral do ambiente:

- Monitorar logs de autenticação.
- Identificar múltiplas tentativas de acesso em curto intervalo de tempo.
- Manter sistemas e serviços atualizados.
- Aplicar o princípio do menor privilégio.
- Realizar auditorias periódicas de segurança.

## 6. Conclusão

A realização dos experimentos demonstrou como mecanismos de autenticação podem ser explorados quando não possuem proteções adequadas.

A adoção de senhas fortes, controles de tentativas, restrições de acesso e monitoramento são medidas importantes para reduzir a exposição a ataques de força bruta e Password Spraying.
