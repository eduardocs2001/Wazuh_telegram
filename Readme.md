
# Configuração da Integração Custom Telegram no Wazuh

## :lock: Permissões

```bash
chmod 750 /var/ossec/integrations/custom-telegram
chown root:wazuh /var/ossec/integrations/custom-telegram
```

## :page_facing_up: Configuração do `ossec.conf`

Adicione a seguinte configuração ao arquivo `ossec.conf`:

```xml
<integration>
    <name>custom-telegram</name>
    <hook_url>https://api.telegram.org/bot<YOUR-BOT-TOKEN>/sendMessage</hook_url>
    <level>3</level>
    <alert_format>json</alert_format>
</integration>
```

> **Nota:** Substitua `<YOUR-BOT-TOKEN>` pelo token do seu bot do Telegram e certifique-se de substituir o `CHATID` pelo seu chatid do Telegram no código correspondente.
