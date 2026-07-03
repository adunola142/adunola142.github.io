I haven't posted here in almost a year. Not because nothing was happening — because everything was. Here's what I've been heads-down building in Nigeria's fintech and payments space.

Most people don't realise how fragmented POS hardware is. Every terminal manufacturer — HorizonPay, Topwise, Dspread, Morefun — ships its own SDK, its own quirks, its own way of talking to the card reader, the printer, the PIN pad. If your product needs to run on more than one terminal brand (and in Nigeria, it usually does), you end up rewriting the same payment logic three or four times.

So I built OctopusTMS: a single Android SDK that abstracts HorizonPay, Topwise, and Dspread terminals behind one unified API. It auto-detects the device at runtime and handles EMV/contactless transactions, PIN pad key injection (TMK/TPK/TSK), and receipt printing — so the app layer never has to care which terminal it's running on. I followed it up with a second SDK integrating Morefun terminals for EMV, RuPay, Mifare/NFC card reading, and QR payments.

Alongside that, I've been shipping the products that sit on top of this infrastructure:
→ Macropay — virtual accounts, payment processing, and a POS app with Mifare tap-and-pay
→ Loop — a cooperative/microfinance app with loan management and interbank transfers
→ LUTH Patient App — hospital bill payments (RRR invoices) and telemedicine for Lagos University Teaching Hospital
→ MRA SWzone — estate management with visitor tokens, emergency alerts, and community services

Different domains, same underlying skill: making payment infrastructure that's reliable enough for real money moving through real hardware.

Back to sharing more regularly. More builds to come.

#Fintech #Nigeria #PaymentsTechnology #POS #Flutter #MobileDevelopment #AndroidDevelopment
