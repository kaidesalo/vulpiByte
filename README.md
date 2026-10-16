# Kaide Salo - Software Engineer Portfolio

A responsive portfolio with a server-side contact form.

- Edit identity and page copy in 'index.html'.
- Edit concept projects and browser interactions in 'styles.css'.
- Design tokens and responsive layouts live in '/assets/'.
- Project visuals and self-hosted fonts live in '/assets/'.
- Build with 'node scripts/build-site.mjs'. This will embed assets in the dependency-free Worker and writes 'dist/server/index.js' plus hosting manifest.

The contact form submits to the same-origin server endpoint. The recipient is then read from the secret runtime value of 'CONTACT-RECIPIENT' and is never sent to the browser. The server then forwards messages with FormSubmit. FormSubmit requires a one-time confirmation before delivery can work. Failed or unconfirmed deliveries return an error, the interface preserves the message for retry. No submitted message content is then logged.

Configure runtime secrets through Sites.

