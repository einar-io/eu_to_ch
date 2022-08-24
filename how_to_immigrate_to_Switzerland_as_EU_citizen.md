How to Immigrate to Switzerland as EU Citizen
=============================================

Here are my notes and recommendations on the process.  They are specific to Zug.  If you encounter any discrepancy, [please let me know](https://github.com/einar-io/eu_to_ch/pulls).


Processes and dependencies
--------------------------


```haskell
do
	Arbeitsvertrag <- getJob
	(Mietvertrag, Maybe Untermietebestädigung) <- rentRoom Arbeitsvertrag
	AufenhaltsbevilligungB <- visitGemeinde Mietvertrag Untermietebestädigung BirthCertificate Arbeitsvertrag
	InsuranceNumber <- getHealthInsurance AufenhaltsbevilligungB
	Aufenhaltskarte <- notifyGemeinde InsuranceNumber
	(IBAN, DebitCard) <- getBankAccount Arbeitsvertrag AufenhaltsbevilligungB Passport
	salary <- getSalary IBAN
	CHDriversLicence <- visitPolice EUDriversLicence
	buyStuff DebitCard Food
where
	getSalary = sendMail Secretary IBAN (getAddress Mietvertrag)
```

Definitions
-----------

- `Arbeitsvertrag`: Work contract.
- `Mietvertrag`: Renting contract. Comes in two flavours: `Hauptmietvertrag` and `Untermietvertrag`.
- `Hauptmieter`: (primary) tenant
- `Untermieter`: subtenant. [get this standard contract](https://www.mieterverband.ch/dam/jcr:5aa1368f-0532-4fd0-ad71-404076d2b260/2019_Untermietvertrag-Wohnraeume_mp_interaktiv.pdf)
- `Untermietebestädigung`: if you sublet, you need a written confirmation from the owner that you are lawfully subletting.
- `Aufenhaltsbevilligung`: Residence permit. I got a B permit.
- `Aufenhaltskarte`: Plastic card you can put in your wallet, so you are no longer legally obliged to have to carry your passport on you at all times.
- `Gemeinde`: Municipality. You will go to [Amt für Migration](https://www.zg.ch/behoerden/sicherheitsdirektion/amt-fur-migration), Aabachstrasse 1, 6301 Zug, T +41 41 728 50 50, info.afm@zg.ch


Deadlines
---------

- You "allegedly" have to get the `AufenhaltsbevilligungB` before you start working, so get the ball rolling now. Engage with the `Gemeinde` - they are there to help you with the process.
- You have about 3 months to sign up for mandatory health insurance and report it to the `Gemeinde`. I got a personal reminder (Nice!) via email, which I then just replied to with my insurance number.
- You have to swap your driver's licence within 1 year.


Personal recommendations based on my preferences and research
-------------------------------------------------------------

1. Get a Hauptmieter contract. If you are subletting (Untermietung), they will give you work permit for 1 year, which you likely can get renewed every year as long as you work. If you are primary tenant (Hauptmieter), you get 5 years.
2. Get a place with A/C and consider beforehand if you need parking. Parking is usually a separate contract that costs from 60CHF/month and up.
3. Get [Sanitas](https://www.sanitas.com/en/private-customers.html) health insurance with maximum deductible of 2500CHF for 200CHF/month.
4. Get [Neon bank](https://www.neon-free.ch/en/).
5. Keep your mobile phone subscription from home, but make sure you have EU roaming.
6. If you want German lessons you want to take them at the Migros Klubschule.  You can take an [online placement test](https://www.klubschule.ch/Angebote/Sprachen/Deutschkurse#tab=tab2) here (~20 min) and see a list of available courses.  If you already speak German and/or want to immigrate more permanently, you should consider their Schweizerdeutsch courses as well and furthermore, volunteer at your local fire brigade.
7. Join the group [Meeting new Friends in Zug](https://www.meetup.com/meeting-new-friends-in-zug/) and socialise.

Transportation
--------------

1. Get SBB app.
2. The first time you pass through a Swiss Railway SBB (Zurich or Zug) sign up for a [Halbtax](https://www.sbb.ch/en/travelcards-and-tickets/railpasses/half-fare-travelcard.html) Abo (subscription) for 185CHF.  Then all train tickets will cost half for a year.
3. If you plan to use the train regularly get a Monatsabo: ~67CHF/month
4. If not, and you occasionally buy a train ticket, and you want to travel twice or more on the same day, buy a Tageskarte instead of an Einzelbillet.
