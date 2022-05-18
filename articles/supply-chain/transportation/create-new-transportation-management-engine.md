---
title: Stofna nýja flutningsstjórnunarvél
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja flutningsstjórnunarvél í Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be52c6afb66e88b36f3b2cdf5af14e17b3d3005f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678123"
---
# <a name="create-a-new-transportation-management-engine"></a>Stofna nýja flutningsstjórnunarvél

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig eigi að stofna nýja flutningsstjórnunarvél í Dynamics 365 Supply Chain Management. 

Flutningsstjórnunarvélar (TMS) skilgreina rökin sem eru notuð til að búa til og vinna flutningstaxta í Flutningsstjórnun. Supply Chain Management býður upp á nokkrar mismunandi gerðir véla sem reikna út mismunandi færibreytur á borð við taxta, flutningstíma og fjölda svæða sem farið verður í gegnum við flutning. Þessi grein útskýrir hvernig á að nota þróunarumhverfi Microsoft Visual Studio saman með þróunarverkfærum Supply Chain Management til að stofna og setja upp nýja TMS-vél og síðan hvernig á að setja upp vélina í Operations. Frekari upplýsingar um vélarnar er að finna í [Flutningsstjórnunarvélar](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Búa til nýja TMS-vél

Í þessum hluta er útskýrt hvernig á að búa til klasasafn sem er með innleiðingu TMS-vélar og hvernig á að vísa í það úr líkani Supply Chain Management.

1. Til að setja nýju vélarnar í gang verður þú að vera með líkan sem inniheldur vélarnar. Á valmyndinni **Dynamics 365** &gt; **Stjórnun líkans** skal smella á **Búa til líkan** til að búa til nýtt líkan. Á fyrstu síðu leiðsagnarforritsins **Búa til líkan** skal gefa líkaninu heitið **TMSEngines**. 

   [![Líkan búið til.](./media/012.png)](./media/012.png)

2. Á næstu síðu skal velja **Búa til nýjan pakka**. 

   [![Nýr pakki búinn til.](./media/021.png)](./media/021.png)

3. Á næstu síðu skal velja líkanið **ApplicationSuite** til að vísa í. (Líkanið **ApplicationPlatform** er valið fyrirfram.) 

   [![Að velja líkanið til að vísa í.](./media/032.png)](./media/032.png)

4. Á næstu síðu skal smella á **Ljúka** til að staðfesta stofnun nýs líkans. 

   [![Lokið við stofnun líkans.](./media/042.png)](./media/042.png)

5. Í nýrri lausn skal stofna nýtt verk Supply Chain Management og gefa því heitið **TMSThirdParty**. Í eiginleikum verksins skal stilla líkan verksins á **TMSEngines**.
6. Bættu nýju C\# klasasafni við lausnina þína og nefndu það **ThirdPartyTMSEngines**.
7. Í ThirdPartyTMSEngines-verkinu skal bæta tilvísunum við samsetningar Supply Chain Management:
   -   Forritasamstæður sem virkja X++ gerðir sem á að vísa í. Þessar samsetningar er hægt að finna á eftirfarandi staðsetningum. \[Rót pakka\] er slóð staðsetningarinnar þar sem allar uppsettar samsetningar eru geymdar, t.d. C:\\Packages.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Framework-samsetningar sem gera kleift að fá aðgang að gögnum, LINQ og öðrum eiginleikum. Allar þessar samsetningar er að finna í \[Rót pakka\]\\hólf.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   Kjarnasamsetning TMS (sem inniheldur vélar) og grunnsamsetning TMS (sem inniheldur hjálpara, fasta, klasaskilgreiningar gagnaflutnings og svo framvegis). Þessar samsetningar er hægt að finna á eftirfarandi staðsetningum.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Endurnefndu C\# klasann sem er sjálfkrafa búinn til í verkinu ThirdPartyTMSEngines í **SampleRatingEngine**.
9. Innleiddu vélina. Vegna þess að við erum að búa til taxtavél í þessu dæmi erfum við úr grunnklasanum fyrir taxtavélar. Grunnklasinn innleiðir mest af viðmóti taxtavélarinnar (**TMSFwkIRateEngine**). Við þurfum bara að innleiða taxtaaðferðina. Til að hafa dæmið einfalt látum við aðferðina skrá harðkóðaðan taxta upp á 100. Hægt er að búa til vélar sem innleiða hvað sem er af viðmótum vélarinnar, t.d. **TMSFwkIAccessorialEngine**. Öll viðmót vélarinnar eru skilgreind í X++.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Hannaðu lausnina.
11. Bættu nýrri tilvísun við verkið TMSThirdParty. Tilvísunin ætti að vísa á verkið ThirdPartyTMSEngines. Lausnin ætti að líta svona út þegar þessu er lokið. 

    [![Lausnin, sem felur í sér tilvísun í verkið TMSThirdParty.](./media/052.png)](./media/052.png)

12. Hannaðu lausnina. Gakktu úr skugga um að nýja safnið birtist í hnútnum **Tilvísanir** í Application Explorer. 

    [![Nýja safnið í tilvísunarhnút Application Explorer.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Setja TMS-vélina upp sem pakka

Ein leið til að setja upp TMS-vélar frá þriðja aðila er í gegnum uppsetningarpakka. Mælt er með þessari aðferð í vinnsluumhverfi. Í þróunarumhverfi er hægt að afrita handvirkt samsetningarnar eins og lýst er í næsta hluta: „Setja upp TMS-vél í Supply Chain Management.“ Til að setja vélina upp sem pakka skal fylgja þessum skrefum.

1. Á valmyndinni **Dynamics 365** &gt; **Uppsetning** skal smella á <strong>Búa til uppsetningarpakka</strong>.
2. Í svarglugganum **Búa til uppsetningarpakka** skal velja líkan TMSEngines og slá inn vefslóðina þar sem á að geyma pakkaskrárnar. 

   [![Líkan TMSEngines valið.](./media/071.png)](./media/071.png)

3. Nú er hægt að setja pakkann upp í viðkomandi umhverfi. Fyrir leiðsögn skal skoða [Setja upp virkjanlegan pakka](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Setja upp TMS-vél í Supply Chain Management

Í þessum hluta er útskýrt hvernig á að setja upp Supply Chain Management til að nota TMS-vél og sýna hvernig nýja vélin sem er búin til er notuð í leit að bestu töxtum. Dæmið í þessum hluta notar sýnigögn USMF-fyrirtækisins.

1. Búðu til nýja vél eins og lýst er í hlutanum „Búa til nýja TMS-vél“.
2. Hannaðu lausnina þína.
3. Afritaðu samsetninguna sem verður til í tvíundarstaðsetningu á þjóni Supply Chain Management: hólf \[AOSWebRoot\]. **Athugaðu:** Þetta skref á aðeins við í þróunarumhverfi. Í vinnsluumhverfi ætti að setja upp í gegnum uppsetningarpakka. Leiðbeiningar eru í hlutanum á undan: „Setja TMS-vélina upp sem pakka.“
4. Í Supply Chain Management, á síðunni **Taxtavélar**, skal búa til nýja taxtavél. Vélin ætti að benda á vélasamstæðuna sem er búin til með því að smíða safn vélaklasans og vélaklasann sem þú innleiddir. 

   [![Ný taxtavél búin til á síðu taxtavélar.](./media/081.png)](./media/081.png)

5. Búðu til farmflytjanda sem notar prufutaxtavélina. Þú þarft ekki að úthluta taxtasniðmáti því vélin okkar notar ekki nein gögn. 

   [![Nýr farmflytjandi stofnaður.](./media/092.png)](./media/092.png)

6. Á síðunni **Vinnusvæði taxtaleiðar** skal smella á **Taxtaleit**. Þú ættir að sjá taxtann 100,00 frá SampleCarrier eins og sýnt er á eftirfarandi skjáskoti. Í þessu dæmi leitum við að bestu töxtum fyrir leið úr vöruhúsi 24 til viðskiptavinar US-004. En úr því að taxtinn er harðkóðaður sérðu alltaf taxtann 100,00.

   [![Taxti vinnusvæðis leiðar.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Ábendingar og góð ráð

- Ef þú notar þróunarverkfæri fyrir Supply Chain Management er gagnlegt að bæta nýju verki við lausnina þína. Ef þú stillir þetta verk sem upphafsverk og setur í gang kembilotu getur þú kembt bæði X++ og C\# kóða í sömu kembilotunni.
- Í hvert skipti sem þú breytir og endurþýðir ThirdPartyTMSEngines-verkið þitt þarftu að afrita handvirkt samsetninguna sem af hlýst í tvíundarstaðsetningunni eða setja upp í gegnum uppsetningarpakka. Annars gætirðu gert keyrslu með útrunninni samsetningu.
- Eftir að þú framkvæmir sértækar TMS-aðgerðir í Supply Chain Management gæti starfsmannaúrvinnsla Internet Information Services (IIS) læst samsetningunni ThirdPartyTMSEngines þannig að ekki verði hægt að uppfæra samsetninguna. Í slíku tilfelli skal endurræsa w3svc-ferlið.

### <a name="whitepaper"></a>Hvítbók

Frekari upplýsingar er að hlaða niður eftirfarandi hvítbók (skrifuð til að styðja AX2012, en gildir einnig fyrir Dynamics 365 Supply Chain Management)

- [Flutningsstjórnunarvélar innleiddar og settar upp](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]