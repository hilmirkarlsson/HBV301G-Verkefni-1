# 📄 Software Requirements Specification (SRS)

## 1. Inngangur
### 1.1 Tilgangur
Settið er app fyrir fólk sem lyftir. Það á að leysa þrennt sem fólk lendir í í ræktinni: að muna ekki hvað var tekið síðast, að vita ekki hvað á að gera í dag og að sjá ekki hvort það er að bæta sig. Þetta skjal lýsir kröfunum sem appið þarf að uppfylla til þess.

### 1.2 Umfang og mörk kerfisins

Innan kerfisins er æfingaskráning (F-1), æfingaplan (F-2) og framfarir (F-3). Utan þess er matur, þolþjálfun, samfélag, þjálfari og greiðslur. Kerfið talar við notandann og við símann sem geymir gögnin og sendir tilkynningar. Æfingasafnið er grátt svæði, ekki ákveðið hvort það er inni eða úti. Nánar í [SDS](../SDS.md).

### 1.3 Skilgreiningar
| Hugtak | Skýring |
|--------|---------|
| SRS | Software Requirements Specification |
| SDS | System Description Specification |
| Sett | Ein lota af endurtekningum í æfingu, t.d. 8 endurtekningar á 80 kg |
| Endurtekning | Ein lyfta innan setts |
| Plan | Vikuáætlun sem segir hvaða æfingar eru hvaða dag, t.d. PPL eða upper/lower |
| Met | Mesta þyngd eða flestar endurtekningar sem notandi hefur náð í æfingu |


### 1.4 Tilvísanir
- Wiegers, K. og Beatty, J. (2013). *Software Requirements*, 3. útg., Microsoft Press. Kafli 1 — tegundir krafna.
- Pohl, K. og Rupp, C. *Requirements Engineering Fundamentals*, kafli 2 — samhengi og mörk kerfis, Figure 2-1.
- ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering," in ISO/IEC/IEEE 29148:2018(E) , vol., no., pp.1-104, 30 Nov. 2018, doi: 10.1109/IEEESTD.2018.8559686.ISO/IEC/IEEE 29

---

## 2. Almenn lýsing
### 2.1 Notendahópar
Allir notendur eru fólk sem lyftir, en þeir eru á mismunandi stað og fá ólíkt út úr appinu:

| Notendahópur | Hvað vantar | Hvað appið gefur |
|---|---|---|
| Alveg byrjandi | Veit ekki hvar á að byrja | Tilbúið plan og hvernig hver æfing er gerð (UR-4) |
| Mætir en veit aldrei hvað á að gera | Ráfar á milli tækja | Sér strax hvað er á dagskrá í dag (UR-3) |
| Mætir en sér engar framfarir | Veit ekki hvort það sem er verið að gera virkar | Sér síðasta sett og söguna svart á hvítu (UR-2, UR-5) |
| Veit alveg hvað á að gera | Vill bara tracka hratt | Skráir sett á nokkrum sekúndum og sér metin sín (UR-1, UR-6) |

Það eru engir stjórnendur, þjálfarar eða aðrir hópar. Notandinn er einn með appið.

### 2.2 Viðskiptaávinningur
Fyrir notandann: færri ástæður til að hætta að mæta. Sá sem veit hvað á að gera mætir, sá sem sér framfarir heldur áfram.

Fyrir þann sem á appið: appið lifir bara ef fólk heldur áfram að nota það. Ef notendahóparnir fjórir fá það sem þá vantar opna þeir appið á hverri æfingu (BREQ-1) og segja vinum sínum frá því (BREQ-2). Þannig vex það án auglýsinga.

---

## 3. Kröfur fyrir kerfið

### 3.1 Viðskiptakröfur
| ID                                        | Titill                    |
|-------------------------------------------|---------------------------|
| [BREQ-1](business_requirements.md#breq-1) | Fólk heldur áfram að nota appið |
| [BREQ-2](business_requirements.md#breq-2) | Fleiri byrja að nota appið |

### 3.2 Kerfiskrafa
| ID                              | Titill                 |
|---------------------------------|------------------------|
| [SR-1](system_requirement.md#sr-1) | [Titill á kerfiskröfu] |

### 3.3 Eiginleikar (Features)
| ID                     | Titill                 |
|------------------------|------------------------|
| [F-1](feature.md#f-1-æfingaskráning) | Æfingaskráning |
| [F-2](feature.md#f-2-æfingaplan) | Æfingaplan |
| [F-3](feature.md#f-3-framfarir) | Framfarir |

### 3.4 Notendakröfur
| ID                                   | Titill                  | Eiginleiki |
|--------------------------------------|-------------------------|------------|
| [UR-1](user_requirement.md#ur-1-skrá-sett-hratt-f-1) | Skrá sett hratt | F-1 |
| [UR-2](user_requirement.md#ur-2-sjá-hvað-ég-gerði-síðast-f-1) | Sjá hvað ég gerði síðast | F-1 |
| [UR-3](user_requirement.md#ur-3-fylgja-plani-í-dag-f-2) | Fylgja plani í dag | F-2 |
| [UR-4](user_requirement.md#ur-4-setja-upp-vikuna-f-2) | Setja upp vikuna | F-2 |
| [UR-5](user_requirement.md#ur-5-sjá-hvort-ég-er-að-bæta-mig-f-3) | Sjá hvort ég er að bæta mig | F-3 |
| [UR-6](user_requirement.md#ur-6-persónuleg-met-f-3) | Persónuleg met | F-3 |

### 3.5 Virknikröfur
| ID                                          | Titill                                      | Notendakrafa |
|---------------------------------------------|---------------------------------------------|--------------|
| [FR-1](functional_requirement.md#fr-1) | Skrá sett á einum skjá | UR-1 |
| [FR-2](functional_requirement.md#fr-2) | Muna síðasta sett | UR-1 |
| [FR-3](functional_requirement.md#fr-3) | Næsta sett með einum smelli | UR-1 |
| [FR-4](functional_requirement.md#fr-4) | Sjá hvað notandi tók síðast | UR-2 |
| [FR-5](functional_requirement.md#fr-5) | Sjá hvenær notandi tók æfinguna síðast | UR-2 |
| [FR-6](functional_requirement.md#fr-6) | Sjá hvort settið er þyngra en síðast | UR-2 |
| [FR-7](functional_requirement.md#fr-7) | Sjá hvað er á dagskrá í dag | UR-3 |
| [FR-8](functional_requirement.md#fr-8) | Klára æfingu og fara í næstu | UR-3 |
| [FR-9](functional_requirement.md#fr-9) | Hvíldardagur | UR-3 |
| [FR-10](functional_requirement.md#fr-10) | Tilbúin plön | UR-4 |
| [FR-11](functional_requirement.md#fr-11) | Velja hvað maður kemst oft | UR-4 |
| [FR-12](functional_requirement.md#fr-12) | Sjá hvernig æfingin er gerð | UR-4 |
| [FR-13](functional_requirement.md#fr-13) | Saga hverrar æfingar | UR-5 |
| [FR-14](functional_requirement.md#fr-14) | Sjá hvort notandi er að bæta sig | UR-5 |
| [FR-15](functional_requirement.md#fr-15) | Velja tímabil | UR-5 |
| [FR-16](functional_requirement.md#fr-16) | Halda utan um met | UR-6 |
| [FR-17](functional_requirement.md#fr-17) | Láta vita þegar notandi slær met | UR-6 |
| [FR-18](functional_requirement.md#fr-18) | Öll metin á einum stað | UR-6 |

### 3.6 Viðskiptareglur
| ID                                  | Titill                     |
|-------------------------------------|----------------------------|
| [BRG-1](business_rule.md#brg-1-notendagögn-eign-notanda) | Notendagögn eign notanda |
| [BRG-2](business_rule.md#brg-2-aðgengismál) | Aðgengismál |

### 3.7 Gæðaeiginleikar
| ID                                      | Titill                     |
|-----------------------------------------|----------------------------|
| [QA-1](quality_attribute.md#qa-1)       | [Gæðaeiginleiki, titill]   |
| [QA-2](quality_attribute.md#qa-2)       | [Gæðaeiginleiki, titill]   |

### 3.8 Takmarkanir
| ID                              | Titill                |
|---------------------------------|-----------------------|
| [C-1](constraint.md#c-1)        | [Takmörkun, titill]   |
| [C-2](constraint.md#c-2)        | [Takmörkun, titill]   |

### 3.9 Ytri skil (Interfaces)
| ID                                      | Titill                |
|-----------------------------------------|-----------------------|
| [UI-1](external_interface.md#ui-1)      | [Ytri skil, titill]   |
| [UI-2](external_interface.md#ui-2)      | [Ytri skil, titill]   |

---

## 4. Viðaukar
### 4.1 Orðalisti
Sjá 1.3.

### 4.2 Samþykktir
- Kennari: ____________________  
- Nemandi: ____________________
