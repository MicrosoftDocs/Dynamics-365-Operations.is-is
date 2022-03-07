---
title: Kröfur um vélbúnaðarþörf fyrir staðbundin umhverfi
description: Þetta efnisatriði tilgreinir kröfur um vélbúnaðarþörf fyrir staðbundin umhverfi.
author: sericks007
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 443b80e44a90a68610fbb2bb5a5f4b6b7d545fa7ad772edb3672972fa82f8cbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763435"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>Kröfur um vélbúnaðarþörf fyrir staðbundin umhverfi

[!include [banner](../includes/banner.md)]

Áður en byrjað er á ferlinu fyrir vélbúnaðar- og innviðaþörf fyrir staðbundið umhverfi skaltu kynna þér [Kerfiskröfur fyrir uppsetningu í skýi](system-requirements.md) og [Leiðbeiningar um uppsetningu og virkjun](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) til að fá góðan skilning á undirliggjandi innviðum.

> [!NOTE]
> Hugaðu sérstaklega að bestu starfsvenjum kerfisuppsetningar fyrir hámarksafköst.

Þegar þú hefur skoðað fylgiskjölin geturðu hafið það ferli að meta færslutengt og samtíma notandamagn og meta stærðarþörf umhverfisins þíns byggt á meðaltals kjarnaafköstum.

## <a name="factors-that-affect-sizing"></a>Þættir sem hafa áhrif á stærðarþörf.

Allir þættir sem eru sýndir í eftirfarandi skýringarmynd hafa áhrif á stærðarþörf. Því ítarlegri upplýsinga sem er safnað, þeim mun nákvæmara er hægt að ákvarða stærðarþörf. Líklegt er að vélbúnaðarþörf, án stuðningsgagna, sé röng. Algjörar lágmarkskröfur fyrir nauðsynleg gögn eru hámarks millifærslulína hleðslu á klst.

[![Vélbúnaðarþörf fyrir staðbundin umhverfi.](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Skoðað frá vinstri til hægri er fyrsti og mikilvægasti þátturinn sem þarf til að meta stærðarþörf nákvæmlega er færslusnið eða færsluframsetning. Mikilvægt er að finna alltaf hámarks færslumagn á hverja klukkustund. Ef það eru mörg hámarkstímabil þarf að skilgreina þessi tímabil nákvæmlega.

Um leið og þú skilur álagið sem hefur áhrif á þína innviði þarftu líka að skilja þessa þætti betur:

- **Færslur** - Venjulega hafa færslur ákveðna toppa yfir daginn/vikuna. Þetta fer aðallega eftir gerð færslunnar. Tíma- og kostnaðarfærslur sýna yfirleitt hámarkspunkta einu sinni í hverri viku viku, á meðan sölupantanafærslur koma oft margar saman með samþættingu eða jafnóðum inn yfir daginn.
- **Fjöldi samtíma notenda** – Fjöldi samtíma notenda er næstmikilvægasti þátturinn varðandi stærðarþörf. Þú getur ekki fengið ábyggilegt mat á stærðarþörf byggt á fjölda samtíma notenda, svo ef það eru einu gögnin sem þú hefur skaltu áætla fjöldann, og skoða þetta aftur þegar þú hefur meiri gögn. Nákvæm skilgreining á samtíma notendum þýðir að:

    - Nefndir notendur eru ekki samtíma notendur.
    - Samtíma notendur eru alltaf hlutmengi nefndra notenda. 
    - Hámarksvinnuálag skilgreinir hámarks samvinnslu fyrir stærðarþörf.

    Skilyrði fyrir samtíma notendur er að notandinn uppfylli öll eftirfarandi skilyrði:

    - Innskráður.
    - Vinnur í færslum/fyrirspurnum þegar talning fer fram.
    - Ekki aðgerðalaus seta.

- **Gagnasamsetning** – Þetta snýst aðallega um hvernig kerfið þitt er uppsett og skilgreint. Til dæmis hve marga lögaðila þú hefur, hve mörg atriði, hve mörg uppskriftarstig, og hve flókið öryggiskerfið þitt er. Hver þessara þátta gæti haft lítil áhrif á afköst, svo hægt er að vega upp á móti þeim snjöllum ákvörðunum hvað varðar innviði.
- **Viðbætur** – Sérsnið geta verið einföld eða flókin. Fjöldi sérsniða og eðli flækjustigs og notkunar hefur mismunandi áhrif á stærð þeirra innviða sem þarf. Fyrir flóknar sérstillingar er ráðlagt að framkvæma afkastamat til að tryggja að þær séu ekki aðeins prófuð fyrir skilvirkni en einnig til að auka skilning á þörfum innviða. Þetta er enn mikilvægara þegar viðbætur eru ekki kóðaðar í samræmi við bestu venjur fyrir afköst og kvarðanleika.
- **Skýrslugerð og greiningar** – Þessir þættir fela yfirleitt í sér að keyra þungar fyrirspurnir við ýmsa gagnagrunna í kerfinu. Skilningur á og lægri tíðni dýrra skýrslna hjálpar þér að skilja áhrif þeirra.
- **Lausnir þriðja aðila** – Þessar lausnir, eins og ISV-lausnir, hafa sömu áhrif og meðmæli og viðbætur.

## <a name="sizing-your-environment"></a>Stærðir í umhverfinu

Til að skilja stærðarkröfur þarftu að vita hámarksmagns færslna sem þú þarft að vinna úr. Flest aukakerfi, eins og Management Reporter eða SSRS, eru ekki eins nauðsynleg. Vegna þess er að mestu einblínt á AOS og SQL Server í þessu skjali.

> [!NOTE]
> Almennt víkka reikningslög út og þau ætti að setja upp sem N+1, sem þýðir að ef þrjú AOS eru áætluð er því fjórða bætt við. Gagnagrunnslagið ætti að vera sett upp sem Alltaf mjög tiltækt.

## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Stærðir

- 3000 til 15.000 færslulínur á klst. í hverjum kjarna í DB þjóni.
- Dæmigert AOS á móti SQL kjarnahlutfall 3:1 fyrir aðal SQL Server. Aukakjarna gæti þurft byggt á valinni grunnstillingu fyrir mikinn tiltækileika.

    - Vinnsla á aðgerðum sem setja mikið álag á gagnagrunna gæti minnkað þetta í 2:1.

- Eftirfarandi þættir hafa áhrif á tilbrigði:

    - Stillingar færibreyta í notkun.
    - Stig viðbóta.
    - Notkun viðbótarvirkni, eins og gagnagrunnsskrár og viðvarana. Mjög mikil gagnagrunnsskráning dregur enn frekar úr afköstum á klst. í hverjum kjarna undir 3000 línur.
    - Flækjustig gagnasamsetningar – Einfaldur bókhaldslykill á móti ítarlegum bókhaldslykli hefur áhrif á afköst (svo dæmi sé tekið).
    - Framsetning færslu.
    - 2 GB til 16 GB minni fyrir hvern kjarna.
    - Viðbótargagnagrunnar á DB þjóni eins og Management reporter og SSRS gagnagrunnar.
    - Tímabundið DB = 15% af DB stærð með jafnmörgum skrár og efnislegir örgjörvar.
    - SAN stærð og afköst byggð á heildarmagni/-notkun samtíma færslna.

### <a name="high-availability"></a>Mikill tiltækileiki

Mælt er með að notast alltaf við SQL Server í annaðhvort klasa- eða speglunaruppsetningu. Annar SQL hnúturinn ætti að hafa sama fjölda kjarna og aðalhnúturinn.

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory samsteypuþjónusta (AD FS)

Fyrir AD FS stærðarþörf skal sjá [Fylgiskjöl fyrir afkastagetu þjóns AD FS](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

[Stærðatöflureiknir](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) er í boði til að áætla fjölda tilvika í þinni virkjun.

## <a name="aos-online-and-batch"></a>AOS (á netinu og runa)

### <a name="sizing"></a>Stærðir

- Stærðir eftir færslumagni/notkun

    - 2000 til 6000 línur í kjarna
    - 16 GB fyrir hvert tilvik
    - Staðlaður kassi - 4 til 24 kjarnar
    - 10 til 15 Enterprise notendur í hverjum kjarna
    - 15 til 25 Activity notendur í hverjum kjarna
    - 25 til 50 Hópmeðlimir í hverjum kjarna

- Runa

    - 1 til 4 runuþræðir í hverjum kjarna
    - Stærð byggð á framsetningu runuglugga

- Athugaðu að AOS, gagnastjórnun og runa eru á sama hlutverki í Service Fabric. Þú þarft að stækka fyrir þessi þrjú vinnuálög samanlagt og ekki aðgreina þau eins og í Microsoft Dynamics AX 2012.
- Sömu breytileikaþættir fyrir SQL þjóna eiga við hér.

### <a name="high-availability"></a>Mikill tiltækileiki

- Gakktu úr skugga um að þú hafir að minnsta kosti 1 til 2 fleiri AOS tiltæka en þú telur þig þurfa.
- Gakktu úr skugga um að þú hafir að minnsta kosti 3 til 4 sýndarhýsla tiltæka.

## <a name="management-reporter"></a>Management reporter

Í flestum tilvikum, nema þegar notkun er mjög mikil, ættu lágmarkskröfur sem mælt er með þar sem tveir hnútar eru notaðir að virka vel. Aðeins í tilfellum þar sem nottkun er mikil þarf fleiri en tvo hnúta. Skalaðu eftir þörfum.

## <a name="sql-server-reporting-services"></a>SQL Server Reporting Services þjónn

Í almennri útgáfu er aðeins hægt að virkja einn SSRS hnút. Fylgstu með SSRS hnútnum þínum við prófun og fjölgaðu tiltækum kjörnum fyrir SSRS eftir þörfum. Gakktu úr skugga um að þú hafir fyrirframgerðan aukahnút tiltækan á sýndarhýsli sem er öðruvísi en SSRS VM. Þetta er mikilvægt ef upp kemur vandamál með sýndarvél sem hýsir SSRS eða sýndarhýsilinn. Ef þetta er tilfellið þyrfti að skipta þeim út.

Frá og með útgáfu 10.0.17 er mögulegt að skilgreina frekari SSSR-hnúta til að öðlast mikinn tiltækileika. Frekari upplýsingar er að finna í [Skilgreina mikinn tiltækileika fyrir SQL Server Reporting Services (SSRS) hnúta](../../dev-itpro/deployment/onprem-ssrsha.md).

## <a name="environment-orchestrator"></a>Environment Orchestrator

Orchestrator þjónustan er þjónustan sem hefur umsjón með þinni virkjun og tengdum samskiptum við LCS. Þessi þjónusta er notuð sem Service Fabric aðalþjónustua og krefst að minnsta kost þriggja VM. Þessi þjónusta er á sama stað og niðurröðunarþjónusta Service Fabric. Stærðin ætti að miðast við hámarksálag klasans. Nánari upplýsingar er að finna í [Skipuleggðu og undirbúðu virkjun á sjálfstæðum Service Fabric klasa](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="virtualization-and-oversubscription"></a>Sýndaruppsetning og ofáskrift

Mikilvæg þjónusta eins og AOS ætti að vera hýst á sýndarhýslum sem hafa sérstök tilföng til þess – kjarna, minni og disk.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
