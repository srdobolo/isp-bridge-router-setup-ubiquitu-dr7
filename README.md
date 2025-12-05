# MEO FiberGateway GR241AG — Ativar Bridge Mode

## 1. MEO FiberGateway GR241AG

### 1.1 Abrir o Painel de Controlo

1. Premir a tecla Windows
2. Procurar por Control Panel
3. Abrir o Control Panel

### 1.2 Ativar o Telnet Client

1. Ir a Programs
2. Clicar em Turn Windows features on or off
3. Selecionar Telnet Client
4. Clicar em OK

## 2. Aceder ao Router via Telnet

Abrir o **Powershell** ou **Command Prompt** e executar:

```bash
telnet 192.168.1.254
```

Credenciais:

```bash
Login: meo
Password: meo
```

## 3. Ativar o Bridge Mode

```bash
lan/bridge-mode/config --enable=enable
lan/bridge-mode/show
```

## 4. Install UniFi OS Server

<https://ui.com/download>

## 5. Setup VLANs

| VLAN | Nome        | Sub-rede         | Uso                        | Dispositivos                     |
|------|-------------|------------------|-----------------------------|----------------------------------|
| 1    | Default     | 192.168.1.x      | Infraestrutura (sem Wi-Fi) | Router, Switch, AP               |
| 2    | Home        | 192.168.2.x      | Dispositivos pessoais      | iPhones, Laptops, Desktop, PS5, TV Box, Smart TV, Impressora |
| 3    | IoT         | 192.168.3.x      | Equipamentos inteligentes  | Echo Dot (Alexa)                 |
| 99   | Guest       | 192.168.99.x     | Rede de convidados         | Dispositivos de visita           |

## 6. Setup WiFi Networks

## 7. Configure Switchports

## 8. Advanced Security Options

## 9. Zone-based FW Rules
