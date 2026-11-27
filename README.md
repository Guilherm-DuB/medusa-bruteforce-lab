# Simulando Ataques de Força Bruta com Medusa e Kali Linux

Laboratório prático de cibersegurança desenvolvido durante o desafio da **DIO em parceria com o Santander**, com o objetivo de simular ataques de força bruta em ambientes controlados e compreender os riscos relacionados à autenticação por senhas.

## 🎯 Objetivo

Explorar o funcionamento de ataques automatizados de tentativa de credenciais utilizando a ferramenta Medusa no Kali Linux, analisando diferentes serviços e identificando possíveis medidas de proteção.

## 🛠️ Ferramentas e tecnologias

- Kali Linux
- Medusa
- Nmap
- Metasploitable 2
- DVWA
- VirtualBox

## 🧪 Cenários desenvolvidos

| Cenário | Descrição | Status |
|---|---|---|
| FTP | Simulação de força bruta contra serviço FTP | Concluído |
| Web (DVWA) | Teste de autenticação em formulário web | Concluído - resultado inconclusivo |
| SMB | Simulação de Password Spraying | Concluído |

## 📂 Estrutura do projeto

```text
medusa-bruteforce-lab/
├── README.md
├── docs/
│   ├── architecture.md
│   ├── environment.md
│   └── mitigations.md
├── scenarios/
│   ├── ftp/
│   ├── web-dvwa/
│   └── smb/
├── screenshots/
│   ├── ftp/
│   ├── web-dvwa/
│   └── smb/
└── LICENSE
```

## 📚 Documentação

- [Arquitetura do laboratório](docs/architecture.md)
- [Ambiente de testes](docs/environment.md)
- [Medidas de mitigação](docs/mitigations.md)
- [Cenário 1 — FTP](scenarios/ftp/README.md)
- [Cenário 2 — Web DVWA](scenarios/web-dvwa/README.md)
- [Cenário 3 — SMB](scenarios/smb/README.md)

## 🔐 Considerações de segurança

Os testes foram realizados em ambiente virtual controlado, utilizando máquinas destinadas à prática de cibersegurança.

Este projeto possui finalidade exclusivamente educacional. As técnicas demonstradas não devem ser utilizadas contra sistemas sem autorização.

## 👨‍💻 Autor

Estudante de Engenharia da Computação, desenvolvendo conhecimentos práticos em cibersegurança, redes e sistemas Linux.

