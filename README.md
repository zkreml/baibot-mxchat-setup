# 🧠 baibot-mxchat-setup

Kompletní konfigurace AI botů pro MXChat komunitu.

## 📦 YAML konfigurace botů

> 🔐 Všechny YAML soubory najdeš ve složce `agents/`

| Soubor | Popis |
|--------|-------|
| `agents/archosuv-botik.yaml` | Osobní room-local bot, technicky laděný pomocník pro Archose |
| `agents/mxchat-bot.yaml`     | Globální komunitní bot pro všechny místnosti |

## 🛠️ Postup nasazení

### 1. Vytvoř agenty

#### 🧑‍💻 Osobní bot (room-local)

V místnosti:

```plaintext
!bai agent create-room-local openai archosuv-botik
```

Do vlákna vlož obsah `agents/archosuv-botik.yaml` a poté nastav:

```plaintext
!bai config room set-handler catch-all room-local/archosuv-botik
```

#### 🌍 Komunitní bot (globální)

```plaintext
!bai agent create-global openai mxchat-bot
```

Do vlákna vlož obsah `agents/mxchat-bot.yaml` a poté nastav:

```plaintext
!bai config global set-handler catch-all global/mxchat-bot
```

## 🧪 Testování

- Napiš zprávu do místnosti s botem
- Nahraj hlasovku (přepis funguje)
- Ověř konfiguraci pomocí:

```plaintext
!bai config status
```

## 🧼 Tipy

- Boti se dají upravovat znovuvytvořením s novým YAML

## 📁 Složky v repozitáři

```
baibot-mxchat-setup/
├── agents/
│   ├── archosuv-botik.yaml
│   └── mxchat-bot.yaml
├── README.md
├── howto/               ← (budoucí návody a příklady)
└── troubleshooting.md   ← (typické chyby a jejich řešení)
```

