# Arquitetura do Laboratório

## 1. Visão geral

O laboratório foi desenvolvido utilizando máquinas virtuais no VirtualBox, com o objetivo de simular ataques de força bruta em um ambiente controlado.

A comunicação entre as máquinas ocorre por meio de uma rede Host-only.

## 2. Componentes do laboratório

| Máquina | Função | Endereço IP |
|---|---|---|
| Kali Linux | Máquina atacante | 192.168.56.101 |
| Metasploitable 2 | Máquina-alvo | 192.168.56.102 |
| DVWA | Aplicação web vulnerável | Hospedada no ambiente de testes |

## 3. Arquitetura da rede

- **Virtualização:** Oracle VirtualBox.
- **Tipo de rede:** Host-only.
- **Máquina atacante:** Kali Linux.
- **Máquina-alvo:** Metasploitable 2.

## 4. Diagrama da arquitetura

```text
       LABORATÓRIO DE CIBERSEGURANÇA
                 VirtualBox
                      |
              Rede Host-only
                      |
          -----------------------
          |                     |
      Kali Linux          Metasploitable 2
   192.168.56.101          192.168.56.102
       Atacante                 Alvo
                                |
                         Serviços vulneráveis
                         FTP / SMB / HTTP
                                |
                              DVWA
```

## 5. Observações

O ambiente foi configurado para fins educacionais, permitindo a execução de testes de autenticação em serviços e aplicações vulneráveis sem envolver sistemas externos.

Os endereços IP apresentados correspondem às máquinas utilizadas durante os testes do laboratório.
