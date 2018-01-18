---
title: "Úrræðaleit vegna innflutnings bankayfirlitsskrár"
description: "Það er mikilvægt að bankayfirlitsskráin frá bankanum samsvari útliti sem Microsoft Dynamics 365 for Finance and Operations, Enterprise edition styður. Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt. Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður. Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni. Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4feb77bf0031494dfd456c23c632a264c96f0e43
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="bank-statement-file-import-troubleshooting"></a>Úrræðaleit vegna innflutnings bankayfirlitsskrár

[!include[banner](../includes/banner.md)]


Það er mikilvægt að bankayfirlitsskráin frá bankanum samsvari útliti sem Microsoft Dynamics 365 for Finance and Operations, Enterprise edition styður. Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt. Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður. Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni. Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu.

<a name="what-is-the-error"></a>Hver er villan?
------------------

Þegar þú hefur reynt að flytja inn bankayfirlitsskránni, skaltu fara í vinnslusögu gagnastjórnunar og í Gögn og upplýsingar um framkvæmd til að finna villuna. Villan getur hjálpað til með því vísa til yfirlits, stöðu eða uppgjörslínu. Hins vegar er ólíklegt að hún veiti nægar upplýsingar til að auðvelda að auðkenna svæði eða einingu sem veldur vandamálinu.

## <a name="what-are-the-differences"></a>Hver er munurinn?
Berðu saman skilgreiningu útlits bankaskrár við innflutningsskilgreiningu Finance and Operations og taktu eftir öllu misræmi í reitum og einingum. Berðu saman bankayfirlitsskrána við tengda sýnisskrá Finance and Operations. Í ISO20022 skrárnar ætti að vera auðvelt að sjá mismun.

## <a name="transformations"></a>Umbreytingar
Yfirleitt, verður að framkvæma breytinguna í einni af þremur umbreytingum. Hver umbreyting er skrifuð fyrir tiltekna staðla.

| Nafn tilfangs                                         | Skrárnafn                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_í\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_í\_Afstemming\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_í\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Kembing umbreytinga
### <a name="adjust-the-bai2-and-mt940-files"></a>Leiðrétta BAI2 og MT940 skrár

BAI2 og MT940 skrár eru skrár byggðar á texta og þarfnast leiðréttingar til að virkja kembingu Extensible Stylesheet Language-Umbreytinga (XSL-umbreyting). Forritið gerir þessa leiðréttingu þegar skrá er innflutt.

1.  Stofna xml-skrá, og afrita eftirfarandi texta í það.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Afrita innihald bankayfirlitsskrár og líma þau í xml-skrána þannig að þær skipta út **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Kemba XSL-umbreytingu

Nánari upplýsingar, sjá <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Ræsa Microsoft Visual Studio.
2.  Stofnið nýtt stjórnborðsforrit.
3.  Opnið viðeigandi XSL-umbreytingu.
4.  Smellt er á XLS-umbreytingu og skilgreiningarsíðu hennar.
5.  Stilltu ílagið á staðsetningu bankayfirlitsskrár.
6.  Skilgreina staðsetningu og skrárnafn fyrir úttak.
7.  Stilltu nauðsynlega rofpunkta.
8.  Á valmyndinni, smelltu á **XML** &gt; **Byrja XSLT kembingu**.

### <a name="format-the-xslt-output"></a>Sníða XLST-úttak

Þegar umbreytingin er keyrð, stofnar hún úttaksskrá sem hægt er að skoða í Visual Studio. Notið Ctrl + A, Ctrl + K og Ctrl + D til að sníða til úttaksskránni á fjótlegan hátt.

### <a name="adjust-the-transformation"></a>Stilla umbreytingu

Stilla umbreytingu til að fá viðeigandi svæði eða einingu í bankayfirlitsskránni. Varpaðu svo þeim reit eða einingu á viðeigandi einingu Finance and Operations.

### <a name="debitcredit-indicator"></a>Vísir fyrir debet/kredit

Stundum gætu debet verið flutt inn sem kredit og kredit verið flutt inn sem debet. Til að leysa þetta vandamál verður að breyta viðkomandi XSL-umbreytingu. Ef bankayfirlit koma úr mörgum bönkum, skal tryggja að þau noti allir sama nálgun fyrir debet/kredit, eða stofna aðskilinn umbreytingar.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-sniðmát
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit-sniðmát
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-sniðmát

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Dæmi um bankayfirlitssnið og tæknilegar útlit
Hér að neðan eru dæmi um skilgreiningar tæknilegs útlits fyrir innflutningsskrár ítarlegrar bankaafstemmingar og þriggja tengdum skrám bankayfirlits: Þú getur sótt dæmi um skrár og tæknilegar lýsingar hingað: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Skilgreining tæknilegs útlits                             | Dæmi bankayfirlitsskránni          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |






