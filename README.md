```
const twilio = require('twilio');

const accountSid = 'your_account_sid';
const authToken = 'your_auth_token';
const client = new twilio(accountSid, authToken);

const whatsappNumber = 'your_whatsapp_number';

client.messages
  .create({
    from: whatsappNumber,
    body: 'Halo! Saya bot WhatsApp.',
  })
  .then((message) => console.log(message.sid))
  .done();
```

