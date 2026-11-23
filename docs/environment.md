# Ambiente de Testes

## 1. Visão geral

O ambiente de testes foi configurado utilizando máquinas virtuais no Oracle VirtualBox, permitindo a realização de experimentos práticos de cibersegurança em uma rede isolada.

## 2. Ferramentas utilizadas

| Ferramenta | Finalidade |
|---|---|
| Kali Linux | Sistema operacional utilizado para executar os testes |
| Medusa | Ferramenta utilizada para simulação de ataques de força bruta |
| Nmap | Identificação de hosts e serviços disponíveis |
| Metasploitable 2 | Máquina virtual vulnerável utilizada como alvo |
| DVWA | Aplicação web vulnerável para testes de autenticação |
| Oracle VirtualBox | Software de virtualização |

## 3. Configuração da rede

A comunicação entre as máquinas do laboratório utiliza uma rede do tipo Host-only.

| Máquina | Endereço IP |
|---|---|
| Kali Linux | 192.168.56.101 |
| Metasploitable 2 | 192.168.56.102 |

## 4. Serviços analisados

Durante o reconhecimento do ambiente, foram identificados os seguintes serviços na máquina Metasploitable 2:

- FTP — Porta 21
- SSH — Porta 22
- HTTP — Porta 80
- SMB — Portas 139 e 445

## 5. Organização dos testes

Os experimentos foram divididos em três cenários:

1. Testes de autenticação no serviço FTP.
2. Testes de autenticação em formulário web utilizando DVWA.
3. Testes de autenticação no serviço SMB.

## 6. Observações

O ambiente foi utilizado exclusivamente para atividades educacionais e experimentos controlados de cibersegurança.

As configurações e ferramentas descritas correspondem aos recursos utilizados no laboratório.
