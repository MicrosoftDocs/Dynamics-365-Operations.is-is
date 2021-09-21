---
title: Úrræðaleit í beinni samstillingarvandamál
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál með beinni samstillingu.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 73a226d10c951179fd9f3bc2aed4a70efcc7f020
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466245"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Úrræðaleit í beinni samstillingarvandamál

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Microsoft Dataverse. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með beinni samstillingu.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Í hverjum hluta er útskýrt hvort þörf sé á ákveðnu hlutverki eða tilteknum innskráningarupplýsingum.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Samstilling í rauntíma sýnir villu þegar þú býrð til línu

Eftirfarandi villuboð kunna að birtast þegar lína er stofnuð í Finance and Operations forriti:

*\[{\\"villa\\":{\\"kóði\\":\\"0x80072560\\",\\"skilaboð\\":\\"Notandinn er ekki meðlimur í fyrirtækinu.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*

Til að laga vandann fylgirðu skrefunum í [Kerfiskröfur og forsendur](requirements-and-prerequisites.md). Til að ljúka þessum skrefum verða notendur forrita tvöfaldrar skráningar sem voru búnir til í Dataverse að hafa kerfisstjórarhlutverkið. Sjálfgefið eigendateymi verður einnig að hafa kerfisstjórarhlutverkið.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Samstilling í rauntíma sýnir villu þegar þú reynir að vista töflugögn

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að vista töflugögn í Finance and Operations forriti:

*Ekki hægt að vista breytingarnar í gagnagrunninum. Vinnueining getur ekki gert færslu. Ekki er hægt að skrifa gögn í mælieiningar einingar. Skrifun í UnitOfMeasureEntity mistókst með villuboðin Ekki var hægt að samstilla við mælieiningar einingar.*

Til að laga vandamálið skaltu ganga úr skugga um að forsendur tilvísunargagna séu til í bæði forriti Finance and Operations og Dataverse. Ef til dæmis viðskiptavinafærsla tilheyrir ákveðnum viðskiptavinahópi skaltu ganga úr skugga um að færsla viðskiptavinahópsins sé til í Dataverse.

Fylgdu þessum skrefum ef gögn eru til á báðum stöðum og þú hefur staðfest að vandamálið tengist ekki gögnum.

1. Opnaðu eininguna **DualWriteProjectConfigurationEntity** með því að nota Excel-viðbótina. Til að nota innbótina skaltu virkja hönnunarsnið í Finance and Operations Excel-innbótinni og bæta **DualWriteProjectConfigurationEntity** við vinnublað. Frekari upplýsingar er að finna í [Skoða og uppfæra einingagögn með Excel](../../office-integration/use-excel-add-in.md).
2. Veldu og eyddu færslunum þar sem vandamál koma upp í vörpun tvöfaldrar skráningar og verki. Það verða tvær færslur fyrir hverja vörpun tvöfaldrar skráningar.
3. Birtu breytingarnar með því að nota Excel-innbótina. Þetta skref er mikilvægt vegna þess að það eyðir færslunum úr einingunni og undirliggjandi töflum.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Meðhöndla villur til að lesa eða skrifa réttindi þegar þú býrð til gögn í forriti Finance and Operations

Þú gætir fengið villuboðin „Villa í beiðni“ þegar þú býrð til gögn í forriti Finance and Operations.

![Dæmi um villuboðin Bad Request.](media/error_record_id_source.png)

Til að laga vandamálið verður þú að virkja réttindin sem vantar með því að úthluta réttu öryggishlutverki til teymis í vörpuðum viðskiptaeiningum Dynamics 365 Sales eða Dynamics 365 Customer Service.

1. Í forriti Finance and Operations finnurðu viðskiptaeininguna sem er varpað í gagnasamsetningar tengingarsettinu.

    ![Fyrirtækjavörpun.](media/mapped_business_unit.png)

2. Skráðu þig inn í umhverfið í forriti viðskiptavinar, farðu í **Stilling \> Öryggi** og finndu hóp varpaðrar viðskiptaeiningar.

    ![Hópur varpaðrar viðskiptaeiningar.](media/setting_security_page.png)

3. Opnaðu síðuna fyrir teymið til að gera breytingar og veldu síðan **Stjórna hlutverkum**.

    ![Hnappurinn Stjórna hlutverkum.](media/manage_team_roles.png)

4. Í svarglugganum **Stjórna hlutverkum teymis** skal úthluta hlutverkið sem er með les-/skrifheimild fyrir viðeigandi töflur og velja síðan **Í lagi**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Laga samstillingarvandamál í umhverfi sem er með nýlega breytt Dataverse umhverfi

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið eftirfarandi villuboð þegar þú stofnar gögn í forriti Finance and Operations:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Ekki tókst að mynda farm fyrir eininguna CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Stofnun farms tókst ekki með villunni Ógilt URI: URI er tómt."}\],"isErrorCountUpdated":true}*

Svona líta villuboðin út í forriti viðskiptavinar:

> Óvænt villa kom upp í ISV-kóða. (ErrorType = ClientError) Óvænt undantekning frá viðbót (Keyra): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: tókst ekki að vinna úr einingareikningi - (Tengingartilraun mistókst vegna þess að tengdur aðili svaraði ekki á fullnægjandi hátt eftir nokkurn tíma, eða ekki tókst að koma á tengingu vegna þess að tengdur hýsill svaraði ekki.

Þessi villa kemur upp ef Dataverse umhverfið er endurstillt á rangan hátt þegar reynt er að búa til gögn í Finance and Operations forritinu.

> [!IMPORTANT]
> Ef þú hefur tengt umhverfin aftur verður þú að stöðva allar varpanir á einingum áður en þú getur haldið áfram með bragarbótaskrefin.

Til að leysa úr vandamálinu þarf að ljúka skrefum í bæði Dataverse og Finance and Operations forritinu.

1. Fylgdu eftirfarandi skrefum í Finance and Operations forritinu:

    1. Opnaðu eininguna **DualWriteProjectConfigurationEntity** með því að nota Excel-viðbótina. Til að nota innbótina skaltu virkja hönnunarsnið í Finance and Operations Excel-innbótinni og bæta **DualWriteProjectConfigurationEntity** við vinnublað. Frekari upplýsingar er að finna í [Skoða og uppfæra einingagögn með Excel](../../office-integration/use-excel-add-in.md).
    2. Veldu og eyddu færslunum þar sem vandamál koma upp í vörpun tvöfaldrar skráningar og verki. Það verða tvær færslur fyrir hverja vörpun tvöfaldrar skráningar.
    3. Birtu breytingarnar með því að nota Excel-innbótina. Þetta skref er mikilvægt vegna þess að það eyðir færslunum úr einingunni og undirliggjandi töflum.
    4. Til að hjálpa til við að koma í veg fyrir villur þegar þú endurtengir Finance and Operations eða Dataverse umhverfin skaltu ganga úr skugga um að engar stillingar tvöfaldrar skráningar séu lengur til staðar.

2. Í Dataverse skal fylgja eftirfarandi skrefum:

    1. Skráðu þig inn í Dataverse umhverfið þitt (til dæmis `https://*****.crm.dynamics.com/`).
    2. Farðu í **Ítarlegar stillingar** \> **Ítarleg leit**.
    3. Veldu **DualWrite Runtime Configuration**.
    4. Veldu dálkinn til að skoða.
    5. Veldu **Niðurstöður** til að skoða skilgreiningarnar.
    6. Eyddu öllum tilvikum.

3. Fylgdu eftirfarandi skrefum í Finance and Operations forritinu:

    1. Opnaðu eininguna **DualWriteProjectConfigurationEntity** með því að nota Excel-viðbótina. Til að nota innbótina skaltu virkja hönnunarsnið í Finance and Operations Excel-innbótinni og bæta **DualWriteProjectConfigurationEntity** við vinnublað. Frekari upplýsingar er að finna í [Skoða og uppfæra einingagögn með Excel](../../office-integration/use-excel-add-in.md).
    2. Veldu og eyddu færslunum þar sem vandamál koma upp í vörpun tvöfaldrar skráningar og verki. Það verða tvær færslur fyrir hverja vörpun tvöfaldrar skráningar.
    3. Birtu breytingarnar með því að nota Excel-innbótina. Þetta skref er mikilvægt vegna þess að það eyðir færslunum úr einingunni og undirliggjandi töflum.
    4. Til að hjálpa til við að koma í veg fyrir villur þegar þú endurtengir Finance and Operations eða Dataverse umhverfin skaltu ganga úr skugga um að engar stillingar tvöfaldrar skráningar séu lengur til staðar.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Villa í samstillingu í rauntíma eftir að full afritun gagnagrunns hefur verið gerð

Þú gætir fengið eftirfarandi villuboð eftir að þú hefur keyrt fulla afritun gagnagrunns úr einu kerfi í annað og síðan reynt að keyra gagnagrunnsaðgerð:

*SecureConfig Organization (???) passar ekki við raunverulegt CRM Organization (???).*

Villuboðin eru sýnd úr keyrsluviðbót tvöfaldrar skráningar til að tryggja að skilgreining tvöfaldrar skráningar sem er sett upp í einu kerfi geti ekki verið notuð í öðru kerfi.

Til að laga vandamálið skaltu eyða öllum færslum í töflunni **msdyn_dualwritertimeconfig** eftir að þú hefur endurheimt gagnagrunninn. Frekari upplýsingar er að finna í [Aftengja og endurtengja umhverfi fyrir tvöföld skrif](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Vandamál við samstillingu í rauntíma sem koma upp vegna rangrar málskipunar í fyrirspurnarsíu í vörpunum tvöfaldra skrifa

Þótt segð fyrirspurnar fyrir vörpunarsíu tvöfaldra skrifa er setningafræðilega rétt er ekki víst að hún virki sem skyldi. Segð síunnar er í einingu, ekki í einstökum gagnagjafa fyrirspurnarhluta. Því skilar SQL-fyrirspurnin sem er mynduð ekki væntum niðurstöðum.

Eftirfarandi er dæmi.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Þú gætir átt von á því að verk sem eru ekki með neina yfireiningu verði síuð frá. Hinsvegar virkar sían ekki vegna þess að henni er breytt í fyrirspurn sem líkist eftirfarandi dæmi.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Raunveruleg niðurstaða er að `parentProject` reiturinn er metinn á `null`. Hinsvegar er `null` ekki það sama og auður strengur. Vegna þessa misræmis skilar fyrirspurnarsían ekki gildum niðurstöðum.

Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Bættu við reiknuðum dálki sem hægt er að bæta við í viðbótarlíkani og sem er studdur með rökum sem breyta `null` í auðan streng.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Notaðu síuna á nýja reiknaða dálkinn í stað sjálfgefna dálksins.

Til að meta síuna í þróunarumhverfi er hægt að nota eftirfarandi X++ kóða til að staðfesta niðurstöðurnar. Keyra þennan kóða sem sjálfstætt forrit. Hægt er að nota hann til að meta mismunandi gerðir af síum sem eiga við um einingu áður en síurnar eru notaðar í vörpunum tvöfaldra skrifa. Hægt er að keyra fyrirspurnina gagnvart gagnagrunninum til að meta misræmi.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Gögn úr Finance and Operations forritum eru ekki samstillt við Dataverse

Við samstillingu í rauntíma gæti komið upp vandamál þar sem aðeins hluti gagnanna eru samstillt úr Finance and Operations forritum í Dataverse eða gögn eru yfirhöfuð ekki samstillt.

> [!NOTE]
> Þú verður að laga þetta vandamál meðan á þróun stendur.

Áður en hafist er handa við að laga vandamálið skal fara yfir eftirfarandi forsendur:

+ Gakktu úr skugga um að sérsniðnu breytingarnar séu skrifaðar í einni færslu.
+ Viðskiptatilvik og rammi tvöfaldra skrifa meðhöndla ekki `doinsert()`, `doUpdate()` og `recordset()` aðgerðir eða færslur þar sem `skipBusinessEvents(true)` er merkt. Ef kóðinn þinn er inni í þessum aðgerðum verða tvöföld skrif ekki ræst.
+ Viðskiptatilvik verða að vera skráð fyrir gagnagjafann sem er varpað. Sumir gagnagjafar gætu notað ytri tengingu og verið merktir sem skrifvarðir í Finance and Operations forritum. Gagnaveiturnar eru ekki rekjanlegar.
+ Breytingar verða aðeins gerðar ef breytingarnar eru gerðar á vörpuðum reitum. Breytingum á óvörpuðum reitum setja ekki tvöföld skrif af stað.
+ Gakktu úr skugga um að mat á síum gefi gilda niðurstöðu.

### <a name="troubleshooting-steps"></a>Úrræðaleitarskref

1. Farðu yfir reitavarpanir á stjórnandasíðu tvöfaldra skrifa. Ef reit er ekki varpað úr Finance and Operations forritum í Dataverse verða hann ekki rakinn. Í eftirfarandi mynd er til dæmis fylgst með reitnum **Lýsing** úr Dataverse forritum en ekki Finance and Operations forritum. Ekki verður hægt að fylgjast með breytingum á þeim reit í Finance and Operations forritum.

    ![Raktir reitir.](media/live-sync-troubleshooting-1.png)

2. Ákvarðaðu hvort gagnagjafinn er rakinn í skilgreiningu viðskiptatilvika. Í eftirfarandi mynd sem dæmi verða engar breytingar raktar í reitum úr töflunni **DefaultDimensionDAVs** og undirliggjandi töflum. Gagnagjafar sem nota ytri tengingu og eru merktir sem skrifvarðir verða ekki raktir.

    ![Reitur sem er ekki rakinn.](media/live-sync-troubleshooting-2.png)

3. Ákvarðaðu hvort varpaðir töflureitir muni birtast í töflunni **BUSINESSEVENTSDEFINITION** eins og sýnt er á eftirfarandi mynd. Ef þú finnur ekki reitinn sem leitað er að í niðurstöðu fyrirspurnarinnar verður hann ekki ræstur með tvöföldum skrifum.

    ![Rakinn reitur í töflunni.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Dæmi

Í Finance and Operations forritum er uppfærsla á aðsetrinu fyrir tengiliðafærslu, en breyting á aðsetri er ekki samstillt við Dataverse. Þessar aðstæður koma upp vegna þess að engin færsla í töflunni **BusinessEventsDefinition** er með samsetningu af töflunni sem um ræðir og einingunni. Taflan **LogisticsPostalAddress** er nánar tiltekið ekki beinn gagnagjafi fyrir eininguna **smmContactpersonCDSV2Entity**. Einingin **smmContactpersonCDSV2Entity** er með **smmContactPersonV2Entity** sem gagnagjafann og **smmContactPersonV2Entity** er í staðinn með **LogisticsPostalAddressBaseEntity** sem gagnagjafa. Taflan **LogisticsPostalAddress** er gagnagjafinn fyrir **LogisticsPostalAddressBaseEntity**.

Svipaðar aðstæður geta komið upp í sumum óhefðbundnum mynstrum á borð við mál þar sem taflan sem verið er að breyta í Finance and Operations forritum er ekki augljóslega tengd við eininguna sem geymir hana. Til dæmis er aðalaðsetrið reiknað í einingunni **smmContactPersonCDSV2Entity**. Rammi tvöfaldra skrifa reynir að ákvarða hvernig breyting í undirliggjandi töflu er varpað aftur í einingar. Oftast nægir þessi aðferð. Í sumum tilvikum er tengillinn svo flókinn að maður þarf að vera nákvæmur. Ganga verður úr skugga um að **RecId** tengdrar töflu sé í boði beint úr einingunni. Síðan skal bæta við ákveðinni aðferð til að fylgjast með breytingum á töflunni.

Sem dæmi skal fara yfir aðferðina **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()**. **CustCustomerV3entity** og **VendVendorV2Entity** hefur verið breytt til að meðhöndla þessar aðstæður.

Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Bættu **PrimaryPostalAddressRecId** reitnum við eininguna **smmContactPersonV2Entity**. Gerðu hann að innri reit.

    ![Reit bætt við smmContactPersonV2Entity eininguna.](media/Troubleshoot_live_sync_issue_1.png)

2. Bættu sama reitnum við **smmContactPersonCDSV2Entity** eininguna.

    ![Reit bætt við smmContactPersonCDSV2Entity eininguna.](media/Troubleshoot_live_sync_issue_2.png)

3. Bættu eftirfarandi aðferð við **smmContactPersonCDSV2Entity** klasann.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Samstilltu gagnagrunninn og smíðaðu forritið.
5. Stöðvaðu allar varpanir tvöfaldra skrifa sem eru búnar til í einingunni **smmContactPersonCDSV2Entity**.
6. Opna kortið. Þú ættir að sjá nýju töfluna (**LogisticsPostalAddress** í þessu dæmi) sem þú byrjaðir að fylgjast með því að nota **RefTableName** dálkinn fyrir línuna þar sem gildið **refentityname** jafngildir **smmContactPersonCDSV2Entity** í töflunni **BusinessEventsDefinition**.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Villa þegar þú stofnar færslu þar sem margar færslur eru sendar úr Finance and Operations forriti til Dataverse í sömu rununni

Fyrir allar færslur býr Finance and Operations forrit til gögn í runu og sendir þau sem runu til Dataverse. Ef tvær færslur eru búnar til sem hluti af sömu færslunni, og þær vísa hvor á aðra, gætir þú fengið villuboð sem líkjast eftirfarandi dæmi í Finance and Operations forritinu:

*Ekki er hægt að skrifa gögn í einingu aaa_fundingsources. Ekki er hægt að fletta upp ebecsfs_contracts með gildum {PC00...}. Ekki er hægt að fletta upp aaa_fundingsources með gildum {PC00...}. Skrif í aaa_fundingsources mistókst með villuboðum Undantekningarskilaboð: Fjartengdur þjónn skilaði villu: (400) Villa í beiðni.*

Til að laga vandamálið skaltu búa til einingavensl í Finance and Operations forritinu til að gefa til kynna að einingarnar tvær séu tengdar hvor annarri og að tengdu færslurnar séu meðhöndlaðar í sömu færslunni.

## <a name="enable-verbose-logging-of-error-messages"></a>Virkja fjölorða skráningu villuboða

Í Finance and Operations forriti gætir þú rekist á villur sem tengjast Dataverse umhverfinu. Villuboðin innihalda ekki endilega heildartexta skilaboðanna eða önnur viðeigandi gögn. Til að fá frekari upplýsingar er hægt að virkja fjölorða skráningu með því að stilla flaggið **IsDebugMode** sem er til staðar í einingunni **DualWriteProjectConfigurationEntity** í öllum verkskilgreiningum í Finance and Operations forritum.

1. Opnaðu eininguna **DualWriteProjectConfigurationEntity** með því að nota Excel-viðbótina. Til að nota innbótina skaltu virkja hönnunarsnið í Finance and Operations Excel-innbótinni og bæta **DualWriteProjectConfigurationEntity** við vinnublað. Frekari upplýsingar er að finna í [Skoða og uppfæra einingagögn með Excel](../../office-integration/use-excel-add-in.md).
2. Stilltu flaggið **IsDebugMode** á **Já** í verkinu.
3. Keyra aðstæður.
4. Fjölorðir kladdar eru fáanlegir í töflunni **DualWriteErrorLog**. Notaðu eftirfarandi vefslóð til að fletta upp gögnum í vafra töflunnar: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Til að ná í fleiri kladda í kembistillingu skaltu setja upp uppfærsluna í [KB 4595434 (Leiðrétting fyrir auð gildi sem er fjölgað í samstillingu í rauntíma fyrir tvöföld skrif)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Villa þegar þú bætir við aðsetri fyrir viðskiptavin eða tengilið

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að bæta aðsetri fyrir viðskiptavin eða tengilið í Finance and Operations forritum eða Dataverse:

*Ekki tókst að skrifa gögn í eininguna msdyn_partypostaladdresses. Skrif í DirPartyPostalAddressLocationCDSEntity mistókst með villuboðum Beiðni mistókst með stöðukóðanum BadRequest og CDS-villukóðanum : 0x80040265 svarskilaboð: Villa kom upp í viðbótinni. Færsla sem hefur eiginleikagildi staðsetningarauðkennis er þegar til staðar. Staðsetningarkenni einingarlykils krefst þess að þetta safn eiginda innihaldi einkvæm gildi. Veldu einkvæm gildi og reyndu aftur.*

Til að laga vandamálið skal setja upp útgáfu skipulagspakka tvöfaldra skrifa (2.2.2.60) þannig að lyklarnir í töflunni **Aðsetur** eru skilgreindir eins og sýnt er í eftirfarandi töflu.

| Eiginleiki | Virði |
|---|---|
| Birtingarheiti | **Staðsetningarlykill** |
| Nafn | **msdyn_locationkey** |
| Svæði | **msdyn_locationid**, **parentid** |
| Staða | **Í gangi** |
| Kerfisverk | Autt |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Villa þegar viðskiptavini er bætt við í Dataverse

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að bæta við viðskiptavini í Dataverse:

*„RecordError0“:“Skrif mistókust fyrir einingu Viðskiptavinir V3 með óþekktri undantekningu - Aðilafærsla finnst ekki fyrir aðilagerð „Fyrirtæki““}.*

Þegar viðskiptavinur er stofnaður í Dataverse er nýtt aðilanúmer búið til. Villuboðin eru sýnd þegar færsla viðskiptavinar ásamt aðilanum er samstillt í Finance and Operations forritum, en þegar er til staðar færsla viðskiptavinar sem er með annað aðilanúmer.

Til að leysa úr vandamálinu skaltu finna viðskiptavininn í gegnum uppflettingu aðila. Ef viðskiptavinurinn er ekki til skaltu búa til nýja færslu viðskiptavinar. Ef viðskiptavinurinn er ekki til skaltu nota núverandi aðila til að stofna nýja færslu viðskiptavinar.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Villa þegar nýr viðskiptavinur, lánardrottinn eða tengiliður í Dataverse er búinn til

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að búa til nýjan viðskiptavin, lánardrottin eða tengilið í Dataverse:

*Ekki er hægt að uppfæra gerð aðila úr „DirOrganization“ í „DirPerson“; þess í stað ætti að eyða út þeim aðila sem þegar er skráður og bæta við skráningu með nýrri gerð.*

Í Dataverse er númeraröð í töflunni **msdyn_party**. Þegar lykill er stofnaður í Dataverse er nýr aðili búinn til (til dæmis **Party-001** af gerðinni **Fyrirtæki**). Þessi gögn eru send til Finance and Operations forritsins. Ef Dataverse umhverfið er endurstillt eða Finance and Operations umhverfið tengt öðru Dataverse umhverfi og síðan er ný tengiliðafærsla stofnuð í Dataverse verður nýtt gildi fyrir aðila sem byrjar á **Party-001** búið til. Að þessu sinni verður aðilafærslan sem er stofnuð að **Party-001** af gerðinni **Einstaklingur**. Þegar þessi gögn eru samstillt sýna Finance and Operations forritin fyrri villuboðin vegna þess að aðilafærslan **Party-001** af gerðinni **Fyrirtæki** er þegar til.

Til að laga vandamálið skal breyta sjálfvirkri númeraröðinni fyrir reitinn **msdyn_partynumber** í töflunni **msdyn_party** í Dataverse í aðra sjálfvirka númeraröð.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Vandamál með afköst vegna vörpunar viðskiptavinar eða tengiliðar

Þú gætir bætt afköst samstillingar í rauntíma að einhverju leyti fyrir viðskiptavini og tengiliði með því að sérstilla aðferðina **getEntityDataSourceToFieldMapping** (í einingunni **CustCustomerV3Entity**) og aðferðina **getEntityDataSourceToFieldMapping** (í einingunni **smmContactPersonCDSV2Entity**). Þessar sérstillingar draga úr fjöldi færslna í töflunni **BusinessEventsDefinition**. Þessi fækkun á fjölda færslna fækkar fjölda tilvika sem koma upp.

Aðferðin **getEntityDataSourceToFieldMapping** í einingunni **CustCustomerV3Entity** gengur úr skugga um að uppfærsla á rafrænu aðsetri viðskiptavinar eða póstfangi setur af stað viðskiptatilvik þannig að uppfærð gögn verði send til Dataverse. Ef þú notar ekki alla reitina og þarft ekki upplýsingarnar í tvöföldum skrifum skaltu setja inn athugasemd í viðeigandi línur í aðferðinni. Hver rakinn reitur og tafla sem bætt er við þessa aðferð bætir við færslu í töflunni **BusinessEventsDefinition** fyrir samsetningu raktrar töflu og rakinnar einingar.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Á svipaðan hátt gengur aðferðin **getEntityDataSourceToFieldMapping** í einingunni **smmContactPersonCDSV2Entity** úr skugga um að uppfærsla á rafrænu aðsetri tengiliðar eða póstfangi setur af stað viðskiptatilvik þannig að uppfærð gögn verði send til Dataverse. Í aðferðinni er hægt að skrifa athugasemdir í línurnar fyrir alla reiti sem ekki eru notaðir.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Eftir að aðferðirnar hafa verið uppfærðar skal fylgja þessum skrefum.

1. Samstilltu gagnagrunninn og smíðaðu forritið.
2. Stöðvaðu allar varpanir tvöfaldra skrifa í einingunum **smmContactPersonCDSV2Entity** og **CustCustomerV3Entity**.
3. Opna kortin. Þú ættir að sjá færri færslur í einingunum **smmContactPersonCDSV2Entity** og **CustCustomerV3Entity** og töflunni **BusinessEventsDefinition** og afköstin gætu aukist að einhverju leyti.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
