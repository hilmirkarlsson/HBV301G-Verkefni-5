# Árekstrar — tvö ólík pör gæðakrafna

Kröfurnar eru í [gæðakröfunum](quality-attributes.md) og GÆ-1 er í [planguage.md](planguage.md).

## Par 1

- **Auðkenni krafna:** GÆ-1 og GÆ-5
- **Aðstæður og mögulegur árekstur (2–3 setningar):** Til að ná 90% sameiginlegum kóða í GÆ-5 skrifum við appið einu sinni í Flutter eða React Native og það keyrir svo bæði á iOS og Android. App sem er skrifað svona er oft hægara en app sem er skrifað bara fyrir iOS eða bara fyrir Android. Á 4 ára gömlum síma gæti þá tekið meira en 1 sekúndu að skrá sett og þá stenst GÆ-1 ekki.
- **Tillaga að lausn:** Við skrifum appið í Flutter eða React Native og mælum strax hvað tekur langan tíma að skrá sett á 4 ára gömlum síma eins og METER í GÆ-1 segir. Ef það tekur meira en 1 sekúndu skrifum við bara þann hluta appsins sem vistar settið sér fyrir iOS og sér fyrir Android. Sá hluti er lítill svo áfram er að minnsta kosti 90% af kóðanum sameiginlegur.
- **Forgangsröðun eða málamiðlun og rök út frá þörfum hagsmunaaðila og áhættu:** GÆ-1 gengur fyrir því notandi skráir mörg sett á hverri æfingu og ef það er alltaf bið hættir notandi að nota appið. GÆ-5 skiptir mestu fyrir okkur sem skrifum appið því þá þarf ekki að skrifa allt tvisvar. Með þessari lausn standast báðar kröfurnar og það eina sem við töpum er að lítill hluti appsins er skrifaður tvisvar.
- **Breytt krafa, ef við á (auðkenni og ástæða):** Engin. Báðar kröfurnar standast með lausninni.

## Par 2

- **Auðkenni krafna:** GÆ-1 og GÆ-3
- **Aðstæður og mögulegur árekstur (2–3 setningar):** Öruggasta leiðin til að ekkert tapist í GÆ-3 er að appið bíði eftir að netþjónninn staðfesti að settið sé komið áður en það birtist skráð. Í World Class er oft lélegt net og á Tjarnarvöllum er 4G lélegt svo staðfestingin tekur oft meira en 1 sekúndu. Þá stenst GÆ-1 ekki og notandi hættir að nota appið og fer í notes. 
- **Tillaga að lausn:** Settið er fyrst vistað á símanum og birtist strax skráð á skjánum. Appið sendir það svo á netþjóninn um leið og netið leyfir og reynir aftur þangað til netþjónninn hefur staðfest það. Settið er ekki tekið af símanum fyrr en sú staðfesting er komin.
- **Forgangsröðun eða málamiðlun og rök út frá þörfum hagsmunaaðila og áhættu:** Notandi þarf hvort tveggja og hvorug krafan er gefin eftir. GÆ-1 er mæld þar til settið birtist á skjánum og GÆ-3 er mæld þar til settið er komið á netþjóninn svo báðar standast. Áhættan er að notandi haldi að settið sé öruggt þegar það er bara á símanum. Þess vegna sýnir appið lítið merki við sett sem eru ekki komin á netþjóninn og varar notanda við ef notandi reynir að skrá sig út á meðan.
- **Breytt krafa, ef við á (auðkenni og ástæða):** Engin. Lausnin er þegar skráð í BASE PLATFORM í [GÆ-1](planguage.md) þar sem stendur að settið birtist um leið og það er vistað á símanum þó það sé ekki komið á netþjóninn.
