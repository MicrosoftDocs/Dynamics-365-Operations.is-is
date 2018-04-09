---
title: "Yfirlit yfir Fínstillingarráðgjöf"
description: "Þetta efnisatriði lýsir því hvernig hægt er að nota Fínstillingarráðgjafa til að tryggja sem besta uppsetningu á Microsoft Dynamics 365 for Finance and Operations."
author: roxanadiaconu
manager: AnnBe
ms.date: 03/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: c055c673443255f3e6dda5e1179e1ef28d90e693
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="optimization-advisor-overview"></a>Yfirlit yfir Fínstillingarráðgjöf

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að nota Fínstillingarráðgjafa til að tryggja sem besta uppsetningu á Microsoft Dynamics 365 for Finance and Operations.

## <a name="overview"></a>Yfirlit

Röng grunnstilling og uppsetning á einingu getur haft neikvæð áhrif á framboð á eiginleikum í Finance and Operations, afköstum kerfisins og hnökralausa vinnslu viðskiptaferla. Gæði viðskiptagagna (til dæmis réttmæti, heilleiki og hreinleiki gagna) hefur einnig áhrif á afköst kerfisins og getu fyrirtækisins til ákvarðanatöku, framleiðni og svo framvegis.

Vinnusvæðið **Fínstillingarráðgjöf** er verkfæri sem leyfir kraftnotendum, viðskiptagreinendum, hagnýtum ráðgjöfum og stuðningsaðgerðir í upplýsingatækni að greina vandamál í grunnstillingu á einingu og viðskiptagögnum. Fínstillingarráðgjöf bendir á bestu starfsvenjur við grunnstillingu á einingu og ber kennsl á viðskiptagögn sem eru úrelt eða röng.

Fínstillingarráðgjöf keyrir reglulega safn af reglum um bestu starfsvenjur. Sjálfgefið reglusafn er gefið út ásamt Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0 (apríl 2018). Hins vegar geta notendur einnig stofnað reglur sem eru sérstakar fyrir sérstillingar þeirra, lausnir frá sjálfstæðum hugbúnaðaraðilum og fyrirtækjagögnum. Nánari upplýsingar um hvernig á að stofna reglur eru í [Búa til nýjar reglur](./create-rules-optimization-advisor.md).

Þegar brot á reglu greinist er búið til fínstillingartækifæri sem birtist á vinnusvæðinu **Fínstillingarráðgjöf**. Notandi getur tekið til viðeigandi aðgerða til úrbóta beint frá vinnusvæðinu **Fínstillingarrágjöf**.

Tækifæri geta verið sértæk fyrir tiltekið fyrirtæki eða almennt hentað fyrirtækjum, fer allt eftir gerð uppsetningar og þeirra gagna sem eru sannprófuð. Tækifæri fyrir fyrirtæki almennt er hægt að skoða frá öllum fyrirtækjum. Til að skoða tækifæri fyrir tiltekið fyrirtæki verður fyrst að velja fyrirtækið.

Staðlaðar öryggisreglur gilda um fínstillingartækifæri. Til dæmis eru fínstillingartækifærin sem tengjast grunnstillingu á einingunni **Vöruhúsakerfi** aðeins sýnileg notendum sem hafa aðgang að Vöruhúsakerfi og geta breytt uppsetningu þess.

Þegar gripið er til aðgerða á ákveðnum fínstillingartækifærum reiknar kerfið áhrif tækifærisins á hvað varðar styttingu á keyrslutíma viðskiptaferla. Því miður er þessi eiginleiki ekki tiltækur fyrir öll fínstillingartækifæri.

Til að læra meira um hagræðingarráðgjöf skal horfa á myndskeiðið [Fínstillingarráðgjöf í Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ).

> [!Video https://www.youtube.com/embed/MRsAzgFCUSQ]

## <a name="optimization-rules"></a>Fínstillingarreglur

Til að skoða heildarlista yfir reglur fínstillingarráðgjafar og til að sjá hversu oft reglurnar eru metnar skal fara í **Kerfisstjórnun** &gt; **Reglubundin verkefni** &gt; **Vinna með villuleitarreglu greiningar**. Aðeins reglur sem hafa stöðuna **Virkt** eru metnar. Hægt er að stilla tíðnimatið á **Daglega**, **Vikulega**, **Mánaðarlega** eða **Ótímasett**.

Til að kveikja á mati á ótímasettum reglum eða til að endurmeta reglubundnar reglur utan fyrirframskilgreindrar tímasetningar skal fara í **Kerfisstjórnun** &gt; **Reglubundin verkefni** &gt; **Tímasetja villuleitarreglu greiningar**. Síðan í svarglugganum **Villuleit greiningarreglu** skal velja tíðnimat. Allar reglur sem hafa tilgreinda tíðni verða endurmetnar.

Núverandi sett af fínstillingarreglum má skipta í eftirfarandi flokka.

### <a name="module-configuration-and-setup"></a>Grunnstilling einingar og uppsetning

Uppsetning Vöruhúsakerfis er flókið ferli. Til að auðvelda ferlið hafa nokkrar reglur verið kynntar til að hjálpa til við að sannprófa réttmæti uppsetningarinnar. Til dæmis sannprófar ein regla uppsetningu staðsetningarleiðbeininga vöruhúss fyrir staðsetningar á föstum afurðarafbrigðum fyrir sölupantanir eða flutningspantanir.

Til viðbótar athuga sumar reglur hvort eiginleikar sem hafa verið virkjaðir séu í raun notaðir. Til dæmis ákvarðar ein reglan hvort verið sé að nota eininguna **Aðaláætlanagerð**. Ef reglan ákvarðar að þú sért ekki að nota eininguna er fínstillingartækifæri búið til sem stingur upp á að slökkt verði á aðaláætlanagerðinni.

### <a name="system-configuration"></a>Kerfisgrunnstilling

Ef tiltekin virkni sem stjórnað er með skilgreiningarlykli er ekki notuð er fínstillingartækifæri búið til sem stingur upp á að slökkt verði á skilgreiningarlyklinum. Dæmi um skilgreiningarlykla eru: **Framleiðsluþyngd**, **Fjárhagsáætlunargerð**, **Verkefni** og **Samþykktur lánardrottnalisti**.

### <a name="business-data-consistency-and-cleanup"></a>Samræmi og hreinsun viðskiptagagna

Ef aðalgögn eru ekki rétt (t.d. ef þú ert með umreikninga á mælieiningu fyrir einingar sem ekki hafa verið skilgreindar, eða ef þú ert umreikninga á mælieininingum sem hafa deilingu með 0 \[núll\]), er búið til fínstillingartækifæri sem stingur upp á að gögnin verði leiðrétti. 

Ef þú ert með of margar færslur runuvinnsluferlis, úreltar vörur, lokaðar lagerbirgðafærslur fyrir vörur með vöruhús virkt, o.s.frv., eða ef þessar færslur og vörur eru of gamlar eru fínstillingartækifæri búin til sem stingur upp á hreinsun á gögnum. Með því að halda gögnum hreinum er hægt að stuðla að bættum heildarafköstum kerfis.

### <a name="best-practices"></a>Bestu venjur

Ef þú ert ekki að keyra viðskiptaferla í samræmi við bestu venjur (til dæmis ef þú keyrir fyrirframlokun birgða áður en birgðir eru lokaðar eða ef þú notar áætlaða runu fyrir runuflutning færslubókar undirfjárhags), munu fínstillingartækifæri láta þig vita af bestu venjunum og biðja þig um að fylgja þeim.

## <a name="optimization-opportunities"></a>Tækifæri til fínstillingar

Til að skoða tækifæri fínstillingar sem eru búin til á meðan á mati á fínstillingarreglum stendur yfir skal opna vinnusvæðið **Fínstillingarráðgjöf**.

Í þessu vinnusvæði geturðu skoðað frekari upplýsingar um tækifæri með því að velja **Frekari upplýsingar**. Ef þú vilt að kerfið gangi til aðgerða og lagfæri uppsetninguna skaltu hreinsa gögnin og svo framvegis, svo að þú þurfir ekki að opna samsvarandi síður sjálfur, skaltu velja **Grípa til aðgerðar**.

Það er ekkert verkflæði fyrir tækifæri til fínstillingar. Eftir að þú hefur valið **Grípa til aðgerðar** eða notað leiðsagnarslóð sem er að finna í svarglugganum **Frekari upplýsingar** hverfur fínstillingartækifærið af listanum. Ef viðeigandi aðgerð leysir ekki vandann að fullu verður tækifærið myndað aftur í næsta skipti sem reglan er metin.

Ef tækifæri á ekki við um hlutverk þitt getur þú valið **Fela frá listanum mínum**. Jafnvel ef kviknar á reglunni á bak við þetta tækifæri aftur seinna, muntu ekki sjá tækifærið á listanum þínum.

Til að gera mat óvirkt á tilgreindum reglum skal velja tækifærið sem reglan bjó til og velja síðan **Gera greiningu óvirka**.

## <a name="see-also"></a>Sjá einnig

[Stofna nýjar reglur](./create-rules-optimization-advisor.md)

[Fínstillingarráðgjöf í Dynamics 365 for Finance and Operations (myndband)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)

