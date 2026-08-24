# DravenCMS Templated Email

Default configuration and shared HTML layout for `salamek/nette-templated-email` in DravenCMS applications.

## Installation

```bash
composer require dravencms/templated-email
```

## Configuration

The bundled defaults use:

- `%appDir%/emailTemplates` for application email templates.
- `%tempDir%/sendEmails` for debug-message storage.
- The package's `@layout.latte` as the common email layout.
- `info@example.com` as the placeholder sender address.

Override the sender before sending mail:

```neon
templatedEmail:
    fromName: Example Application
    fromEmail: no-reply@example.com
```

Application templates belong in `app/emailTemplates` unless `templateStorage` is changed. Refer to `salamek/nette-templated-email` for message creation, variable passing, attachments, and transport usage.

Do not ship the placeholder sender address in production. Keep transport credentials in local or environment-specific configuration.

## License

This package is licensed under the LGPL-3.0-only license.
