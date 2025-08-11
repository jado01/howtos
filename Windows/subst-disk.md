# 🪟 Substituovanie priečinka ako disk vo Windows

Tento návod popisuje, ako vo Windows vytvoriť **substituovaný disk** pomocou príkazu `subst`.

---

## 1️⃣ Dočasné vytvorenie disku

1. Vytvorim si zlozku v PC s nejakym nazvom ktoru chcem pouzivat ako substituovany disk.
		napr. Python - ten chcem pouzivat ako substituovany disk P
2. V tejto zlozke vytvorim bat subor. (standardny textovy subor s priponou .bat)
3. Nazyvem ho napr. spustenie_disku_p.bat
4. Otvorím ho v notepade
5. napisem tam tieto dva subory:
	SUBST P: /d	(za medzerou je dvojbotka)
	SUBST P: .	(za medzerou je dvojbotka)
		- prvý príkaz ma za úlohu prípadnu doposial nastavenú substituciu disku P:
		- druhý príkaz substituuje aktuálnu zložku ako disk P:
6. Subor vlozim do zlozky z ktorej chcem mať substituovaný disk
7. Kedykoľvek súbor spustím, dávka substituuje zložku a , v ktorej je umiestnena, ako
		príslušný disk

---

## 2️⃣ Trvalé vytvorenie disku (pri štarte systému)
🔹 Metóda s .bat súborom

Ak chem mať nastavený disk trvalo spravím nasledovné:
1. Stlačím: win + R
2. Napíšem: shell:startup - otovrí sa priečinok Po spustení/startup
3. Cez prieskumníka otvorím zložku ktorú chem mať ako substituovaný disk a v ňom 
		je vytvorená zložka
4. Pravým tlačidlom myši kliknem na ikonu súboru a pretiahnem do priečinka Po spustení
5. Pustím tlačidlo a otvorí sa ponuka z ktorej vyberiem vytvoriť zástupcu.
6. To je všetko 😊 Aj po reštarte bude substituovaná zložka vytvorená 😘
