# Afleiddar virknikröfur og samþykktarpróf

## VK-1 — Staðfesting og eyðing notendagagna

- **Viðskiptaregla:** [VR-1 Eignarhald gagna](business-rules.md#vr-1).
- **Ferli eða verkefni notanda:** Eyða aðgangi notanda [QA-2 Persónuvernd](https://github.com/hilmirkarlsson/HBV301G-Verkefni-1/blob/main/SRS/quality_attribute.md#qa-2-pers%C3%B3nuvernd).
- **Virknikrafa eða tilvísun í fyrirliggjandi kröfu:** Þegar notandi velur að eyða reikningi sínum skal kerfið krefjast skýrrar staðfestingar. Við staðfestingu skal kerfið eyða öllum persónuupplýsingum og skráðum æfingagögnum notandans varanlega úr geymslu og af netþjóni, skrá notandann út og birta notanda staðfestingarskilaboð. Ef notandi velur að hætta við í staðfestingarglugga skal engum gögnum eytt.
- **Viðbótarforsendur eða tilvísun í sameiginlegar forsendur:** Eyðingin er óafturkræf og engin gögn notandans eru varðveitt í afritum eftir að eyðing hefur verið staðfest.

### SP-1 — leyfilegt eða gilt tilvik

- **Sannreynir:** VK-1
- **Gefið:** Notandi er skráður inn í appið Settið og á skráð æfingagögn í símanum.
- **Þegar:** Notandi velur „Eyða aðganginum mínum" í stillingum og ýtir svo á „Staðfesta að eyða aðgangi“ í staðfestingarglugganum.
- **Þá:** Kerfið eyðir öllum persónu- og æfingagögnum notandans varanlega, skráir notanda út og birtir skilaboðin: „Aðgangi þínum og gögnum hefur verið eytt.“

### SP-2 — óleyfilegt tilvik eða viðeigandi jaðartilvik

- **Sannreynir:** VK-1
- **Gefið:** Notandi er skráður inn í appið Settið og á skráð æfingagögn í símanum.
- **Þegar:** Notandi velur „Eyða aðganginum minum“ í stillingum en ýtir á „Hætta við“ í staðfestingarglugganum.
- **Þá:** Kerfið framkvæmir ekki eyðingu, hvorki á gögnum né aðgangi, lokar staðfestingarglugganum og öll gögn notandans verða áfram aðgengileg óbreytt.

## VK-2 — Greining og merking persónulegs mets

- **Viðskiptaregla :** [VR-2 Skilgreining á persónulegu meti](business-rules.md#vr-2)
- **Ferli eða verkefni notanda:** Skrá æfingu / skoða tölfræði ([UR-6 Persónuleg met](https://github.com/hilmirkarlsson/HBV301G-Verkefni-1/blob/main/SRS/user_requirement.md#ur-6-pers%C3%B3nuleg-met-f-3))
- **Virknikrafa eða tilvísun í fyrirliggjandi kröfu:** Tengist fyrirliggjandi virknikröfu [FR-17 Láta vita þegar notandi slær met](https://github.com/hilmirkarlsson/HBV301G-Verkefni-1/blob/main/SRS/functional_requirement.md#fr-17). Við skráningu á nýju æfingasetti skal kerfið bera saman þyngd og endurtekningar settsins við áður skráð sett notandans í sömu æfingu. Ef settið inniheldur hærri þyngd eða fleiri endurtekningar á sömu þyngd skal kerfið merkja settið sýnilega sem persónulegt met. Uppfylli settið ekki skilyrði VR-2 skal kerfið ekki vista það sem nýtt persónulegt met.
- **Viðbótarforsendur eða tilvísun í sameiginlegar forsendur:** Aðeins staðfest æfingasett (þ.e. ekki upphitunarsett) eru borin saman við fyrri skráningar notandans.

### SP-3 — leyfilegt eða gilt tilvik

- **Sannreynir:** VK-2
- **Gefið:** Notandi á áður skráð met í bekkpressu sem er 100 kg, endurtekið 5 sinnum.
- **Þegar:** Notandi skráir nýtt sett í bekkpressu með inntakinu 105 kg og 5 endurtekningum og ýtir á „Vista sett“.
- **Þá:** Kerfið vistar settið merkt „Persónulegt met“, við settið á skráningarskjánum um leið og settið birtist.

### SP-4 — óleyfilegt tilvik eða viðeigandi jaðartilvik

- **Sannreynir:** VK-2
- **Gefið:** Notandi á áður skráð met í bekkpressu sem er 100 kg, endurtekið 5 sinnum.
- **Þegar:** Notandi skráir nýtt sett í bekkpressu með inntakinu 95 kg og 5 endurtekningum og ýtir á „Vista sett“.
- **Þá:** Kerfið vistar settið en merkir það **ekki** sem persónulegt met.
