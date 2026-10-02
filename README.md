# L4GG Comms Tools

Small web tools for the Lawyers for Good Government communications team, published at https://l4gg-comms.github.io

## Email Converter (converter/)

Turns a Repro Health Digest, Trans Rights Digest or Impact Docket Google Doc into Mailchimp HTML in the house style.

- **No AI.** The conversion is fixed rules written in plain JavaScript inside converter/index.html. There is no model, no API and no server.
- **No outside connections.** Each page sets Content-Security-Policy: default-src 'none', so the browser blocks any attempt to send or load anything from the internet. What you paste stays in your browser tab.
- **Formatting only.** It reads bold, italic, underline, links, bullet levels and font sizes, and applies the newsletter's fonts, sizes, colors and spacing. It never adds, removes, reorders or rewords text. The one change to links is removing the google.com/url?q= wrapper Google Docs adds.
- **It checks itself.** After converting, it re-reads the HTML and compares every word, every link and every italic phrase with the pasted Doc. If anything differs, it shows the spot and disables the Copy button.
- **Every change is tracked.** This repository's history shows who changed the tools, what changed and when.

To review the conversion rules, read the section of converter/index.html that begins L4GG Email Converter - conversion engine.
