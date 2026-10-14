I haven't posted here in almost a year. Not because nothing was happening — because everything was. Here's what I've been heads-down building in Nigeria's fintech and payments space.

Most people don't realise how fragmented POS hardware is. Every terminal manufacturer — HorizonPay, Topwise, Dspread, Morefun — ships its own SDK, its own quirks, its own way of talking to the card reader, the printer, the PIN pad. If your product needs to run on more than one terminal brand (and in Nigeria, it usually does), you end up rewriting the same payment logic three or four times.

So I built OctopusTMS: a single Android SDK that abstracts four terminal OEMs — HorizonPay, Topwise, Dspread (both its POS terminal and card reader), and Morefun — behind one unified API. It auto-detects the device at runtime and handles EMV/contactless transactions, Mifare/NFC/CPU card reading, QR payments, secure PIN pad key injection and encryption key management, and receipt printing — so the app layer never has to care which terminal it's running on.

Alongside that, I've been shipping the products that sit on top of this infrastructure — mobile and backend:
→ Macropay — virtual accounts, payment processing, and a POS app with Mifare tap-and-pay
→ Loop — a cooperative/microfinance app with loan management and interbank transfers
→ LUTH Patient App — Flutter + NestJS, hospital bill payments (RRR invoices) and telemedicine for Lagos University Teaching Hospital
→ MRA SWzone — Flutter + NestJS, estate management with visitor tokens, emergency alerts, and role-based access for residents, security, and admins — live on Google Play and the App Store

Different domains, same underlying skill: making payment infrastructure — and the APIs behind it — reliable enough for real money moving through real hardware.

Back to sharing more regularly. More builds to come.

#Fintech #Nigeria #PaymentsTechnology #POS #Flutter #MobileDevelopment #AndroidDevelopment
