---
layout: base
title: Kontakt
---

<form 
  name="contact" 
  method="POST" 
  netlify-honeypot="non-human"
  data-netlify-recaptcha="true"
  data-netlify="true"
>
  <p style="display: none;">
    <label>Don’t fill this out if you’re human: <input name="non-human" /></label>
  </p>
  <p>
    <label>Dein Name: <input type="text" name="name" /></label>
  </p>
  <p>
    <label>Deine E-Mail: <input type="email" name="email" /></label>
  </p>
  <p>
    <label>Deine Nachricht: <textarea name="message"></textarea></label>
  </p>
  <div data-netlify-recaptcha="true"></div>
  <p>
    <input type="submit" />
  </p>
</form>