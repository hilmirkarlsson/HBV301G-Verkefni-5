# Gæðakröfur — 3 ytri og 2 innri

GÆ-1 er sett fram með PLanguage í [planguage.md](planguage.md). Hinar fjórar eru á almennu máli.

## Ytri gæðaeiginleikar (3)

| Auðkenni | Gæðaeiginleiki | Krafa og aðstæður | Sannreyning | Rökstuðningur og sértækar forsendur |
|---|---|---|---|---|
| GÆ-1 | Afköst (Performance) | Notandi skráir sett í hvíldinni á milli setta. 95% skráninga skulu birtast á skjánum innan 1 sekúndu. Öll krafan er í [planguage.md](planguage.md#gæ-1--afköst-við-skráningu-setts). | Sjá METER í [planguage.md](planguage.md#gæ-1--afköst-við-skráningu-setts). | Sjá rökstuðning í [planguage.md](planguage.md#gæ-1--afköst-við-skráningu-setts). |
| GÆ-2 | Nytsemi (Usability) | Nýr notandi sem hefur aldrei notað Settið opnar appið í ræktinni og ætlar að skrá fyrsta settið sitt. 9 af hverjum 10 nýjum notendum skulu geta skráð fyrsta settið sitt án hjálpar á innan við 60 sekúndum. | Nytsemispróf með 10 manns úr ræktinni sem hafa ekki séð appið. Engin kennsla er gefin. Tíminn er mældur frá því appið opnast þar til settið er skráð og skrifað niður hverjir þurftu hjálp. | Settið á að vera einfalt app og fólk hættir að nota öpp sem eru of flókin. Ef nýr notandi kemst ekki sjálfur í gegnum fyrsta settið eru litlar líkur á að notandi komi aftur. |
| GÆ-3 | Áreiðanleiki (Reliability) | Notandi skráir sett þar sem netsamband er lélegt eða ekkert. Engin skráning má tapast. 100% skráninga sem eru gerðar án nets skulu vera komnar á netþjón innan 5 mínútna eftir að samband kemst aftur á. | Netið er tekið af símanum með flugstillingu og 50 sett skráð. Appinu er lokað einu sinni á meðan. Netið er svo sett aftur á og eftir 5 mínútur er athugað að öll 50 settin séu á netþjóninum í réttri röð. | Ef skráning tapast getur notandi ekki treyst sögunni sinni og sér ekki bætingarnar sínar. **Forsenda okkar:** til dæmis er wifi-ið í World Class lélegt og 4G sambandið á Tjarnarvöllum er líka lélegt svo notandi getur ekki treyst á netið á æfingu. |

## Innri gæðaeiginleikar (2)

| Auðkenni | Gæðaeiginleiki | Krafa og aðstæður | Sannreyning | Rökstuðningur og sértækar forsendur |
|---|---|---|---|---|
| GÆ-4 | Breytanleiki (Modifiability) | Forritari bætir nýrri æfingu eða nýrri tegund af plani við Settið. Ný æfing skal bætast við án þess að breyta kóða heldur bara gögnunum í æfingaskránni. Ný tegund af plani skal bara kalla á breytingu í einni einingu og forritari sem þekkir kóðann skal klára hana á innan við 2 klst. Þá er talið með að skrifa kóðann og prófin en ekki rýni og útgáfa. | Bætt er við einni nýrri æfingu og einni nýrri tegund af plani. Farið er yfir commit-in og athugað hvaða skrár breyttust. Tíminn sem fór í hvora breytingu er skráður. | Plön breytast og notendur biðja um nýjar æfingar svo þetta eru breytingar sem gerast oft. Ef hver breyting tekur langan tíma dregst appið aftur úr. |
| GÆ-5 | Flytjanleiki (Portability) | Settið er gefið út á iOS og Android. Að minnsta kosti 90% af kóðanum skal vera sameiginlegur fyrir bæði stýrikerfin. Virkni sem er til á öðru stýrikerfinu skal vera til á hinu í sömu útgáfu. | Línur kóðans eru taldar og skipt í sameiginlegar og sértækar fyrir hvort stýrikerfi. Sömu samþykktarpróf eru keyrð á iOS og Android og öll þurfa að standast á báðum. | Ef appið virkar bara á einu nær það bara til helmingsins af fólkinu í ræktinni. Ef kóðinn er að mestu sameiginlegur þarf ekki að skrifa allt tvisvar. **Forsenda okkar:** appið er skrifað í ramma sem keyrir á báðum kerfum eins og Flutter eða React Native. |
