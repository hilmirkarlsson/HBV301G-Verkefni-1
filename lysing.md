# Svitna — hvað er þetta?

*Stutt kynning fyrir verkefnisfélaga. Skrifað 3. sept. 2026.*

## Hugmyndin í einni setningu

**Svitna** („að svitna“) er ræktarapp fyrir Ísland: þú mætir í ræktina, smellir einu sinni,
og hópurinn þinn sér að þú mættir. Það er kjarninn. Restin er ofan á honum.

## Þrír hlutar, eitt app

1. **Félagsskapur** — mætingarstimpill, hópar (ræktin þín, liðið þitt), straumur fyrir hópinn og
   fyrir allt Ísland („hverjir eru að púla núna“). Þú velur hver sér mætinguna: hópurinn, allt
   Ísland eða bara þú.
2. **Æfing og matur** — sett skráð með tillögu þjálfarans um næstu þyngd, matardagbók með
   makró-markmiðum, framfarir, skipting vikunnar.
3. **GYMBRO** — gervigreindarþjálfari með persónuleika (vísindalegur, gamli skólinn, eða þar á
   milli), sem þú skírir sjálf/ur. Talar við þig á meðan þú æfir, svarar spurningum, býr til plan.
   Þetta er áskriftarhlutinn.

Markmiðið: **fá fólk til að mæta** — hvatning í gegnum sýnileika, ekki hype. Íslenska fyrst,
fyrir konur og karla jafnt (appið beygir orðin eftir því hvernig þú vilt láta ávarpa þig:
*mætt* / *mættur*).

## Hvar er þetta statt?

- Hönnun valin og teiknuð (stíllinn heitir *Plakat*).
- Appið er til sem frumgerð: allir skjáir virka í vafra á símastærð, gögn vistast á tækinu.
- Ekkert netþjónslag enn — Supabase er skipulagt (sjá `supabase/schema.sql`) en ekki tengt.
- Aldrei keyrt á alvöru síma enn.

## Tæknin, stutt

- **Expo / React Native** (einn kóði fyrir iOS og Android), TypeScript, Expo Router.
- **Supabase** (Postgres, auth, storage) þegar það verður tengt — Frankfurt.
- Kóðinn: `mobile/`. Hönnunin: `design/`. Gagnagrunnur: `supabase/`.

```bash
cd mobile && pnpm install && pnpm start     # w = vafri, eða Expo Go á símanum
```

## Tengingin við HBV301G — Verkefni 1: Tegundir krafna og samhengi

Svitna er **kerfið sem við vinnum með í námskeiðinu**, í öllum sex verkefnunum. Verkefni 1 (skil
7. sept. í Gradescope) biður um:

- **Kröfusöfnun**: hvernig við nálgumst kröfurnar (viðtöl við fólk í ræktinni/liðinu, eigin
  hugmyndavinna), helstu **notendahópar** (byrjendur, vanir, keppnisfólk; líkamsræktarstöðvar
  sem kaupendur) og **viðskiptaávinningur** (fleiri mætingar → betri endurkoma fyrir stöðvarnar).
- **38 kröfur í tilteknum fjölda**: 2 viðskiptakröfur, 1 kerfiskrafa, 3 eiginleikar, 6 notendakröfur
  (2 á eiginleika), 18 virkniskröfur (3 á notendakröfu), 2 viðskiptareglur, 6 óvirkniskröfur
  (2 gæðaeiginleikar, 2 takmarkanir, 2 ytri skil). Eiginleikarnir þrír liggja beint við:
  **mætingin**, **æfingaskráningin**, **þjálfarinn**.
- **Samhengismynd** (Figure 2-1 í Pohl & Rupp): kerfið og mörk þess, hagsmunaaðilar (notandi,
  hópurinn, ræktin, App Store/Play, Supabase, úr/heilsuforrit, gervigreindarþjónusta) — og eitt
  **grátt svæði**: er matvæladagagrunnurinn (Krónan o.fl.) hluti af kerfinu eða samhengi þess?
- **Verkaskipting og Git**: Kanban-borð á repo-inu, Hvannberg sem collaborator, allir gera commit,
  push og pull request.
- **Ígrundun** og **gagnsæisyfirlýsing** um notkun gervigreindar.

Fulla verkefnalýsingin og glósur úr vikum 2–3 eru í Brain-vaultinu:
`2-Areas/School/Fall 2026/5-Verkfræði kröfugreiningar/Efni/Verkefni/Verkefni 1 - Tegundir krafna og samhengi.md`.

## Hvað næst?

1. Setja Svitna-repo-ið upp sem Kanban og bjóða Hvannberg.
2. Skrifa kröfurnar 38 saman — byrja á eiginleikunum þremur og notendakröfunum.
3. Teikna samhengismyndina.
