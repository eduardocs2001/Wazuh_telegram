Permissões:
chmod 750 /var/ossec/integrations/custom-telegram;
chown root:wazuh /var/ossec/integrations/custom-telegram

Ossec.conf:
<integration>
    <name>custom-telegram</name>
    <hook_url>https://api.telegram.org/bot<YOUR-BOT-TOKEN>/sendMessage</hook_url>
    <level>3</level>
    <alert_format>json</alert_format>
  </integration>

No código não esqueça de Substituir o CHATID pelo seu chatid do Telegram!