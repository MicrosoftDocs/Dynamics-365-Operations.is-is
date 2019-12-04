---
title: Yfirlit yfir aðgerðir viðskiptavina
description: Í þessu efnisatriði er að finna yfirlit yfir nýja aðgerðagetu viðskiptavina sem er í boði í smásöluforritinu.
author: bebeale
manager: AnnBe
ms.date: 11/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: fb58022f61f9944d6e385874db1f2342bc111866
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773985"
---
# <a name="clienteling-overview"></a>Yfirlit yfir aðgerðir viðskiptavina

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Margir smásalar, sérstaklega smásalar með dýra sérvöru, vilja að söluaðilar þeirra myndi langtímasambönd við helstu viðskiptavini sína. Búist er við að söluaðilarnir þekki hvað viðskiptavinunum líkar og líkar ekki, kaupsögu þeirra, vöruval og mikilvægar dagsetningar, eins og brúðkaupsafmæli og afmæli. Söluaðilar þurfa stað þar sem þeir geta náð þessum upplýsingum og finna þær auðveldlega þegar þess er krafist. Ef þessar upplýsingar eru tiltækar á stökum skjá geta söluaðilarnir auðveldlega miðað við viðskiptavini sem uppfylla ákveðin skilyrði. Til dæmis geta þeir fundið alla viðskiptavini sem kjósa að kaupa handtöskur, eða viðskiptavini sem hafa mikilvægan viðburð framundan, eins og brúðkaupsafmæli eða afmæli.

## <a name="client-book"></a>Biðlarabók

Í Microsoft Dynamics 365 Retail geta smásalar notað virkni viðskiptavinabókarinnar til að hjálpa starfsfólki verslunarinnar að mynda langtímasambönd við helstu viðskiptavini.

Viðskiptavinabókin inniheldur viðskiptavinakort sem sýna upplýsingar um tengiliði fyrir hvern viðskiptavin ásamt þremur viðbótareiginleikum sem eru skilgreindir af söluaðilanum og stilltir í Retail Headquarters. Söluaðilar geta ákveðið þrjá mikilvægustu hlutina sem söluaðilar ættu að vita um viðskiptavini. Til dæmis gæti skartgripasöluaðili viljað hafa með mikilvægar dagsetningar eins og brúðkaupsafmæli eða afmælisdaga, því þessar dagsetningar eru tilefni þar sem fólk gæti keypt fleiri skartgripi. Að sama skapi gæti tískuverslun viljað hafa með kaupáhuga og vörumerki viðskiptavinarins.

Viðskiptavinabókin gerir söluaðilum einnig kleift að sía listann þannig að hann sýnir aðeins viðskiptavini sem uppfylla ákveðin skilyrði. Til dæmis ef ný lína af skóm er komin í verslunina og söluaðili vill upplýsa viðskiptavini sem vilja kaupa skó. Í þessu tilfelli getur söluaðilinn síað viðskiptavinabókina til að finna viðeigandi viðskiptavini og síðan gripið til frekari aðgerða.

Ef einhverjir viðskiptavinir eru ekki lengur taldir lykilviðskiptavinir af einhverjum ástæðum og ætti því ekki að vera náið stjórnað, geta söluaðilar fjarlægt þá úr viðskiptavinabók sinni.

Sumir smásalar vilja ekki hafa umsjón með viðskiptavinum á söluaðilastigi. Þess í stað vilja þeir hafa umsjón með lista yfir helstu viðskiptavini í versluninni. Þessir smásalar geta skoðað viðskiptavini úr viðskiptavinabókum verslunarinnar. Með því að nota þennan valkost geta smásalar skoðað viðskiptavinina úr viðskiptavinabókum allra söluaðila með heimilisfangabók sem passar við heimilisfangabók núverandi verslunar. Á þennan hátt, ef söluaðili vinnur í mörgum verslunum lögaðila, sýnir viðskiptavinabókin viðskiptavini úr öllum þessum verslunum. Þessi virkni styður viðbótargetu. Til dæmis er hægt að endurúthluta viðskiptavini frá einum söluaðila til annars. Þessi geta er gagnleg þegar söluaðilar eru fluttir eða yfirgefa fyrirtækið.

Hver sölumaður getur verið með eina viðskiptavinabók á hvern lögaðila og söluaðilar geta bætt einum eða fleiri viðskiptavinum við viðskiptavinabókina. Í Retail er aðeins hægt að bæta sérhverjum viðskiptavini við í eina viðskiptavinabók. Hins vegar hyggst Microsoft bæta við virkni sem gerir kleift að einum viðskiptavini sé bætt við margar bækur viðskiptavina.

> [!NOTE]
> Ólíkt leit viðskiptavina, síar viðskiptavinabók ekki viðskiptavinaupplýsingar samkvæmt heimilisfangabókum verslunarinnar.

## <a name="activities-and-notes"></a>Verkþættir og athugasemdir

Netrásir veita smásöluaðilum leiðir til að fræðast um óskir viðskiptavina án þess að krefjast þess að viðskiptavinir gefi þessar upplýsingar skýrt fram. Aftur á móti, þegar viðskiptavinir hafa samskipti við söluaðila í versluninni, deila þeir beinlínis upplýsingum um óskir sínar. Því miður, þessar upplýsingar geta tapast eftir að sölunni er lokið. Ef þessar upplýsingar eru skráðar geta þær hins vegar hjálpað smásöluaðilum að skilja viðskiptavini betur og því hjálpað þeim að veita betri ráðleggingar og betri verslunarupplifun í heild sinni.

Til að fanga mikilvægar upplýsingar sem viðskiptavinir deila, geta söluaðilar ekki aðeins notað eigind viðskiptavinarbókarinnar, heldur einnig notað aðgerðir og athugasemdir. Söluaðilar geta stillt aðgerðategundirnar, svo sem upplýsingar um heimsóknina í versluninni, netfang, símanúmer og stefnumót. Hægt er að skoða athafnir sem söluaðilar búa til á tímalínusniði á sölustað (POS). Einnig er hægt að skoða þau á flipanum **Verkþættir** á síðunni **Allir viðskiptavinir \> Almennt** í Retail Headquarters.

Söluaðilar geta einnig notað athugasemdir til að afla almennra viðskiptavinaupplýsinga sem vísa má í á undan hverjum samskiptum. Þessar athugasemdir eru vistaðar í Retail Headquarters og hægt er að skoða þær á viðskiptavinasniði eða á upplýsingasíðu viðskiptavinar í símaverinu.

> [!NOTE]
> Sem stendur er hægt að skoða allar athugasemdir og verkþætti af öllum söluaðilum sem starfa hjá lögaðilanum og geta skoðað upplýsingasíður viðskiptavina. Athugasemdir og verkþættir takmarkast ekki við söluaðilann sem bætti viðskiptavini við viðskiptavinabókina.

## <a name="integration-with-dynamics-365-customer-insights"></a>Samþætting með Dynamics 365 Customer Insights

Með því að nota forrit Dynamics 365 Customer Insights geta smásalar safnað saman gögnum frá hinum ýmsu kerfum sem viðskiptavinir nota til að hafa samskipti við vörumerki smásalans. Þeir geta síðan notað þessi gögn til að búa til eina sýn á viðskiptavininn og öðlast innsýn. Samþætting viðskiptavinarins við Retail gerir smásölum kleift að velja eina eða fleiri ráðstafanir sem ætti að sýna á viðskiptavinaspjaldinu í viðskiptavinabókinni. Til dæmis geta smásalar notað gögnin í Customer Insights til að reikna „líkindin á svindli“ fyrir viðskiptavin og skilgreina „næst bestu aðgerðina“. Ef þessi gildi eru skilgreind sem ráðstafanir er hægt að sýna þau á viðskiptamannaspjaldinu og geta veitt söluaðilum mikilvægar upplýsingar. Nánari upplýsingar um Customer Insights eru í fylgiskjalinu [Dynamics 365 Customer Insights](https://docs.microsoft.com/dynamics365/ai/customer-insights/overview). Fyrir frekari upplýsingar um ráðstafanir, sjá [Ráðstafanir](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Settu upp viðskiptavinamiðlun

Fylgdu þessum skrefum til að kveikja á viðskiptavinarvirkni í umhverfi þínu.

1. Í vinnusvæðinu **Stjórnun eiginleika** síarðu eiginleikana með einingunni **Smásala og viðskipti**.

    ![Viðskiptavinir í lista yfir eiginleika fyrir eininguna Smásala og viðskipti](./media/Enable_clienteling.png "Viðskiptavinir í lista yfir eiginleika fyrir eininguna Smásala og viðskipti")

2. Kveiktu á eiginleikanum **Viðskiptavinir** með því að velja **Virkja núna**.
3. Á síðunni **Færibreytur smásölu**, á flipanum **Númeraröð**, velurðu línuna **Kenni viðskiptavinarbókar**. Síðan, í reitnum **Kóði númeraraðar** skal velja númeraraðarkóða fyrir hverja tilvísun. Kerfið mun nota þessa númeraröð til að úthluta kenni á viðskiptavinabækur.
4. Veljið **Vista**.
5. Búðu til nýjan eigindahóp sem inniheldur eiginleika sem þú vilt ná fyrir viðskiptavini sem er stjórnað í viðskiptavinabókum. Fyrir leiðbeiningar skal sjá [Eigindi og eigindaflokkar](https://docs.microsoft.com/dynamics365/retail/attribute-attributegroups-lifecycle).

    - Skilgreindu nauðsynlega eiginleika sem **Hægt að fínstilla**. Sölufélagar geta síðan notað þessa eiginleika til að sía viðskiptavinabók sína.
    - Stilltu skjáröð fyrir þessa eiginleika. Þessi skjáröð ákvarðar hvaða eiginleikar ættu að birtast á viðskiptavinaspjaldinu í viðskiptavinabókinni. Skjáröð 1 er talin hærri en skjáröð 2. Þess vegna verður eigindin sem hefur skjáröð 1 sýnd á undan eigindinni sem hefur skjáröð 2.

    > [!NOTE]
    > Þú getur gert Customer Insights aðgengileg af sömu síðu. Samt sem áður verður að búa til auðkenni Azure forrits og leyndarmál, til að sannprófa. (Fyrir upplýsingar um kröfurnar, sjá hlutann [Kveikja á samþættingu Customer Insights við Retail](#turn-on-the-integration-of-customer-insights-with-retail) síðar í þessu efni.) Ef kveikt er á Customer Insights og þú velur eina eða fleiri ráðstafanir sem ætti að sýna á viðskiptavinaspjaldinu, verða þessar ráðstafanir sýndar fyrst. Næst verða eigindahópar viðskiptavinarbókar sýndir, byggðar á skjáröðuninni. Til dæmis, ef þú velur tvo mælikvarða úr Customer Insights, þá verða þeir tveir mælikvarðar og ein eigind viðskiptavinarbókar sýndir á viðskiptavini kortinu. (Einkenni viðskiptavinarbókarinnar sem er sýndur er eiginleiki sem hefur hæstu skjáröð.)

6. Á síðunni **Færibreytur Retail**, á flipanum **Viðskiptavinir**, í reitnum **Eigindahópur viðskiptavinarbókar**, veldu eigindahópinn sem þú bjóst til.

    ![Eigindahópur viðskiptavinabókar valinn](./media/Client%20book%20attributes.png "Eigindahópur viðskiptavinabókar valinn")

7. Til að fanga athafnir sem eiga sér stað í POS skaltu skilgreina aðgerðategundirnar á síðunni **Gerðir verkþátta** (**Retail \> Viðskiptavinir \> Gerðir verkþátta**).

    > [!NOTE]
    > Retail Server dregur upp gerðir verkþátta þegar hann hringir í rauntíma í fyrsta skipti. Eftir að verkþættirnir eru dregnir eru þeir í skyndiminni í nokkrar klukkustundir. Ef þú breytir gerðum verkþátta skaltu bíða þar til skyndiminnið er ekki lengur gilt. Að öðrum kosti, fyrir umhverfi án framleiðslu, skaltu endurræsa þjónustuna Retail Server.

8. Bættu tveimur hnöppum við viðeigandi POS skjáskipulag svo að söluaðilar geti skoðað sína eigin viðskiptavinabók og viðskiptavinabók verslunar. (Viðskiptavinabækur verslunar samanstanda af viðskiptavinum úr öllum viðskiptavinabókum allra söluaðila sem deila heimilisfangaskrá með versluninni.) Samsvarandi aðgerðir eru nefndar **Skoða viðskiptavini í viðskiptavinabók** og **Skoða viðskiptavini úr viðskiptavinabókum verslunar**, hver um sig. Þrjár aðgerðir til viðbótar sem tengjast viðskiptavinabókum eru fáanlegar. Þessar aðgerðir ákvarða hvaða söluaðilar geta bætt við, fjarlægt og endurúthlutað viðskiptavinum úr viðskiptavinabókinni. Þær eru nefndar **Bæta viðskiptavini við viðskiptavinabók**, **Fjarlægja viðskiptavini úr viðskiptavinabók** og **Endurúthluta viðskiptavinum í viðskiptavinabók**, hver um sig.
9. Keyra eftirfarandi dreifingaráætlunarstörf: 1040, 1150, 1110 og 1090.

Eftir að þú hefur lokið þessu ferli geta söluaðilar opnað upplýsingasíðu viðskiptavinar í POS og bætt við viðskiptavini í viðskiptavinabók sína, skoðað og náð verkþáttum og athugasemdum fyrir viðskiptavini og miðað út viðskiptavini með því að nota eigind viðskiptavina og viðskiptavinarbókar til að sía viðskiptavinabók. Eftirfarandi skýringarmynd sýnir dæmi um viðskiptavinabók.

![Dæmi um viðskiptavinabók](./media/client_book.png "Dæmi um viðskiptavinabók")

## <a name="turn-on-the-integration-of-customer-insights-with-retail"></a>Kveiktu á samþættingu Customer Insights við Retail

Til að kveikja á samþættingu Customer Insights við Retail verður þú að ganga úr skugga um að þú sért með virkt tilvik af Customer Insights í leigjanda þar sem Retail er veitt. Þú verður líka að hafa Azure Active Directory (Azure AD) notendareikning sem er með Azure áskrift.

Fylgdu þessum skrefum til að setja samþættinguna upp.

1. Skráðu forrit í Azure gáttina. Þetta forrit verður notuð til sannvottunar með Customer Insights. Fyrir leiðbeiningar skal sjá [Stuttur leiðarvísir: Skráðu forrit á Microsoft kennivettvang](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).
2. Mynda nýtt leyndarmál fyrir forritið. Skrifaðu leyndarmálið og geymdu það á öruggum stað, því þú þarft á því að halda seinna. Veldu einnig gildistíma leyndarmálsins.

    > [!IMPORTANT]
    > Passaðu að þú munir að breyta leyndarmálinu áður en það rennur út. Annars stöðvast samþættingin óvænt.

3. Búðu til Azure lykilgeymslu og vistaðu forritsleyndarmálið. Fyrir leiðbeiningar skal sjá [Stuttur leiðarvísir: Stilla og sækja leyndarmál úr Azure lyklageymslu með Azure vefsíðunni](https://docs.microsoft.com/azure/key-vault/quick-create-portal).
4. Kveiktu á aðgangi að Azure lykilgeymslu úr Retail. Til að ljúka þessu skrefi verður þú að hafa auðkenni umsóknar og leyndarmál. Forritið getur verið sama forrit og þú bjóst til í skrefi 1, eða það getur verið nýtt forrit. (Með öðrum orðum, þú getur notað forritið sem þú bjóst til í skrefi 1 fyrir bæði lykilgeymsluaðgang og þjónustuaðgang Customer Insights, eða þú getur búið til einstakt forrit fyrir hverja tegund aðgangs.) Fyrir leiðbeiningar skal sjá [Geymið helstu skilríki í Azure Stack lykilgeymslunni](https://docs.microsoft.com/azure-stack/user/azure-stack-key-vault-store-credentials?view=azs-1908#create-a-service-principal).
5. Í Retail Headquarters ferðu í **Kerfisstjórnun \> Uppsetning \> Færibreytur lykilgeymslu** og sláðu inn nauðsynlegar upplýsingar um lykilgeymslu. Síðan, í reitnum **Biðlari lyklageymslu**, slærðu inn forritskennið sem þú notaðir í skrefi 4, svo að Retail geti nálgast leyndarmál í lyklageymslunni.
6. Til að bæta forritinu sem þú bjóst til í skrefi 1 á lista yfir örugg forrit (stundum vísað til sem hvítlista) skaltu fara í Customer Insights og veita aðganginn **Skoða** að forritinu. Fyrir leiðbeiningar skal sjá [Heimildir](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-permissions).
7. Í Retail, á síðunni **Færibreytur Retail**, á flipanum **Viðskiptavinir**, á flýtiflipanum **Dynamics 365 Customer Insights**, fylgirðu þessum skrefum:

    1. Í reitinn **Forritskenni** slærðu inn forritskennið sem þú notaðir í skrefi 1.
    2. Í reitinn **Heiti leyndarmáls** slærðu inn heiti leyndarmáls lyklageymslunnar sem þú bjóst til í 5. þrepi.
    3. Stillið valkostinn **Customer Insights** á **Já**. Ef uppsetningin tekst ekki af einhverjum ástæðum, þá færðu villuboð og þessi valkostur verður stilltur á **Nei**.
    4. Þú getur haft mörg umhverfi í Customer Insights, svo sem prófunar- og framleiðsluumhverfi. Í reitinn **Tilvikskenni umhverfis** slærðu inn viðeigandi umhverfi.
    5. Í reitinn **Kenni annars viðskiptavinar** slærðu inn eiginleikann í Customer Insights sem er varpað á reikningsnúmer viðskiptavinarins. (Í Retail er lykilnúmer viðskiptavinar kenni viðskiptavinarins.)
    6. Eiginleikarnir þrír sem eftir eru eru ráðstafanirnar sem verða sýndar á viðskiptavinaspjaldinu í viðskiptavinabókinni. Þú getur valið allt að þrjár ráðstafanir til að sýna á viðskiptavinaspjaldinu. (Hins vegar þarftu ekki að velja neinar ráðstafanir.) Eins og áður sagði sýnir kerfið þessi gildi fyrst og síðan sýnir það gildi fyrir eigindahóp viðskiptavinarbókarinnar.