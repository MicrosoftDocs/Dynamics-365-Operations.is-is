---
title: Common Data Service einingar
description: Microsoft Dynamics 365 Human Resources notar Common Data Service til að gera mögulegt atburðarás fyrir stækkun og samþættingu.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009459"
---
# <a name="common-data-service-entities"></a>Common Data Service einingar

Microsoft Dynamics 365 Human Resources notar Common Data Service til að gera mögulegt atburðarás fyrir stækkun og samþættingu.

Nánari upplýsingar um Common Data Service er að finna í [Hvað er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Eftirfarandi einingar Human Resources eru í boði í Common Data Service.

## <a name="benefit-entities"></a>Fríðindaeiningar

**Útreikningstíðni fríðinda**

| **Reitir**        | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------------|---------------|--------------|----------------|
| Lýsing       | Text          |              | X              |
| Stjórnun tíðni | Valkostur stilltur    | X            | X              |
| Er óbreytanlegt      | Tveir möguleikar   |              | X              |
| Nafn              | Text          | X            | X              |


**Hlutfall útreikninga fyrir fríðindi**

| **Reitir**  | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------|---------------|--------------|----------------|
| Lýsing | Text          |              | X              |
| Nafn        | Text          | X            | X              |
| TierType    | Valkostur stilltur    | X            | X              |


**Upplýsingar um hlutfall útreikninga fyrir fríðindi**

| **Reitir**                             | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|----------------------------------------|----------------|--------------|----------------|
| Upplýsinganúmer um hlutfall útreikninga fyrir fríðindi | Text           | X            | X              |
| Hlutfallskenni útreikninga                    | Leit         | X            | X              |
| Framlagsaðferð                    | Valkostur stilltur     | X            | X              |
| Virkt                              | Einungis dagsetning      | X            | X              |
| Framlag vinnuveitanda                  | Fjöldi aukastafa |              | X              |
| Lok gildistíma                             | Einungis dagsetning      | X            | X              |
| WorkerDeduction                        | Fjöldi aukastafa |              | X              |


**Gerð fríðinda**

| **Reitir**           | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Valkostur stilltur    |              | X              |
| Lýsing          | Text          |              | X              |
| Nafn                 | Text          | X            | X              |
| PayrollCategory      | Valkostur stilltur    |              | X              |


**Fríðindaáætlun**

| **Reitir**                               | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|------------------------------------------|----------------|--------------|----------------|
| Aðferð við takmörkun vanskila                      | Valkostur stilltur     |              | X              |
| Gerð fríðinda                             | Leit         | X            | X              |
| Takmörkunaraðferð framlags                | Valkostur stilltur     |              | X              |
| Framlagsaðferð                      | Valkostur stilltur     |              | X              |
| Gjaldmiðill                                 | Leit         |              | X              |
| Frádráttarforgangur                       | Heiltala   |              | X              |
| Sjálfgefin framlagstakmörkunarupphæð        | Gjaldmiðill       |              | X              |
| Sjálfgefin framlagstakmörkunarupphæð (grunnur) | Gjaldmiðill       |              | X              |
| Sjálfgefið tímabil framlagsmarka        | Valkostur stilltur     |              | X              |
| Sjálfgefin frádráttarmarkaupphæð           | Gjaldmiðill       |              | X              |
| Sjálfgefin frádráttarmarkaupphæð (grunnur)    | Gjaldmiðill       |              | X              |
| Sjálfgefið frádráttarmarkatímabil           | Valkostur stilltur     |              | X              |
| Lýsing                              | Text           |              | X              |
| Gengi                            | Fjöldi aukastafa |              | X              |
| Er viðbótarlaunakeyrsla                | Tveir möguleikar    |              | X              |
| Er tilkynningarskylt samkvæmt Affordable Care Act        | Tveir möguleikar    |              | X              |
| Er vanskilamyndað                      | Tveir möguleikar    |              | X              |
| Er hækkun                              | Tveir möguleikar    |              | X              |
| Er aðal                               | Tveir möguleikar    |              | X              |
| Nafn                                     | Text           | X            | X              |
| Áhrif á launaskrá                           | Valkostur stilltur     |              | X              |
| Starfslokagerð                          | Valkostur stilltur     |              | X              |


**Starfseining**

| **Reitir**                     | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|--------------------------------|----------------|--------------|----------------|
| Breyttur upphafsdagur starfskrafts     | Dagsetning og tími  |              | X              |
| Fyrirt.                          | Leit         | X            | X              |
| Upphæð tilkynningaeiningar vinnuveitanda | Fjöldi aukastafa |              | X              |
| Tilkynningareining vinnuveitanda        | Valkostur stilltur     |              | X              |
| Dagsetning starfsloka            | Dagsetning og tími  |              | X              |
| Starfsnúmer              | Text           | X            | X              |
| Upphafsdagur starfs          | Dagsetning og tími  |              | X              |
| Síðasti vinnudagur              | Dagsetning og tími  |              | X              |
| Dagsetning breytinga                | Dagsetning og tími  |              | X              |
| Gildir frá                     | Dagsetning og tími  | X            | X              |
| Gildir til                       | Dagsetning og tími  |              | X              |
| Starfskraftur                         | Leit         | X            | X              |
| Tilkynningarupphæð starfskrafts           | Fjöldi aukastafa |              | X              |
| Fyrsti starfsdagur starfskrafts             | Dagsetning og tími  |              | X              |
| Gerð starfskrafts                    | Valkostur stilltur     | X            | X              |
| Tilkynningareining starfskrafts          | Valkostur stilltur     |              | X              |

## <a name="worker-entities"></a>Starfskraftaeiningar

**Þjóðernisuppruni**

| **Reitir**         | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|--------------------|---------------|--------------|----------------|
| Lýsing        | Text          |              | X              |
| Heiti þjóðernisuppruna | Text          | X            | X              |


**Tungumál**

| **Reitir**    | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|---------------|---------------|--------------|----------------|
| Lýsing   | Text          |              | X              |
| Tungumálsheiti | Text          | X            | X              |


**Uppgjafahermennskustaða**

| **Reitir**           | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|----------------------|---------------|--------------|----------------|
| Lýsing          | Text          |              | X              |
| Er verndaður uppgjafahermaður | Tveir möguleikar    |              | X              |
| Tungumálsheiti        | Text          | X            | X              |


**Starfskraftur**

| **Reitir**                | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|---------------------------|---------------|--------------|----------------|
| Fæðingardagur                 | Einungis dagsetning     |              | X              |
| Lýsing               | Text          |              | X              |
| Netfang 1           | Netfang         |              | X              |
| Netfang 2           | Netfang         |              | X              |
| Facebook auðkenni         | Text          |              | X              |
| Fornafn                | Text          |              | X              |
| Fullt nafn                 | Text          |              | X              |
| Kyn                    | Valkostur stilltur    |              | X              |
| Myndun                | Text          |              | X              |
| Er netfangstengiliður leyfður  | Tveir möguleikar   |              | X              |
| Er símatengiliður leyfður  | Tveir möguleikar   |              | X              |
| Eftirnafn                 | Text          |              | X              |
| Auðkenni LinkedIn         | Text          |              | X              |
| Yfirmaður                   | Leit        |              | X              |
| Millinafn               | Text          |              | X              |
| Farsími              | Sími         |              | X              |
| Office Graph kennimerki   | Text          |              | X              |
| Aðalnetfang     | Netfang         |              | X              |
| Aðalsími         | Sími         |              | X              |
| Starf                | Text          |              | X              |
| Samfélagsmiðill 1          | Valkostur stilltur    |              | X              |
| Samfélagsmiðill 2          | Valkostur stilltur    |              | X              |
| Auðkenni félagslegs nets 1 | Text          |              | X              |
| Auðkenni félagslegs nets 2 | Text          |              | X              |
| Uppruni                    | Valkostur stilltur    | X            | X              |
| Staða                    | Valkostur stilltur    | X            | X              |
| Sími 1               | Sími         |              | X              |
| Sími 2               | Sími         |              | X              |
| Sími 3               | Sími         |              | X              |
| Auðkenni Twitter          | Text          |              | X              |
| Notandi                      | Leit        |              | X              |
| Vefslóð               | Vefslóð           |              | X              |
| Númer starfskrafts             | Text          | X            | X              |
| Gerð starfskrafts               | Valkostur stilltur    | X            | X              |
| Yomi fornafn           | Text          |              | X              |
| Yomi fullt nafn            | Text          |              | X              |
| Yomi eftirnafn            | Text          |              | X              |
| Yomi millinafn          | Text          |              | X              |


**Aðsetur starfskrafts**

| **Reitir**           | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|----------------------|----------------|--------------|----------------|
| Húsnúmer       | Text           | X            | X              |
| Gerð aðseturs         | Valkostur stilltur     | X            | X              |
| Póststöð                 | Text           |              | X              |
| Land eða svæði    | Text           |              | X              |
| Sýsla               | Text           |              | X              |
| Fax                  | Sími          |              | X              |
| Er æskilegt         | Tveir möguleikar    |              | X              |
| Breiddargráða             | Fjöldi aukastafa |              | X              |
| Lína 1               | Text           |              | X              |
| Lína 2               | Text           |              | X              |
| Lína 3               | Text           |              | X              |
| Lengdargráða            | Fjöldi aukastafa |              | X              |
| Póstnúmer          | Text           |              | X              |
| Póstkassi      | Text           |              | X              |
| Kóði sendingarmáta | Heiltala   |              | X              |
| Fylki eða hérað    | Text           |              | X              |
| Sími 1          | Sími          |              | X              |
| Sími 2          | Sími          |              | X              |
| Sími 3          | Sími          |              | X              |
| UPS-svæði             | Text           |              | X              |
| UTC-mótbókun           | Heiltala   |              | X              |
| Starfskraftur               | Leit         | X            | X              |


**Persónuupplýsingar starfskrafts**

| Reitir                             | Gagnagerð    | Krafa | Hægt að leita |
|------------------------------------|--------------|----------|------------|
| Fæðingarborg                         | Text         |          | X          |
| Fæðingarland/-svæði            | Valkostur stilltur   |          | X          |
| Fæðingardagur                          | Einungis dagsetning    |          | X          |
| Land eða svæði ríkisfangs      | Valkostur stilltur   |          | X          |
| Dánardagur                      | Einungis dagsetning    |          | X          |
| Staðfesting öldungatryggingardags | Einungis dagsetning    |          | X          |
| Menntun                          | Text         |          | X          |
| Þjóðernisuppruni                     | Leit       |          | X          |
| ExpatriateEndDate                  | Einungis dagsetning    |          | X          |
| ExpatriateStartDate                | Einungis dagsetning    |          | X          |
| Fæðingarland eða svæði föður     | Valkostur stilltur   |          | X          |
| Kyn                             | Valkostur stilltur   |          | X          |
| Er óvirkt                        | Tveir möguleikar  |          | X          |
| Er fatlaður uppgjafahermaður                | Tveir möguleikar  |          | X          |
| Er eiga reglur um búsetu erlendis við    | Tveir möguleikar  |          | X          |
| Er námsmaður í fullu námi               | Tveir möguleikar  |          | X          |
| Hjúskaparstaða                     | Valkostur stilltur   |          | X          |
| Lokadagsetning herþjónustu          | Einungis dagsetning    |          | X          |
| Upphafsdagsetning herþjónustu        | Einungis dagsetning    |          | X          |
| Fæðingarland eða svæði móður     | Valkostur stilltur   |          | X          |
| Land eða svæði þjóðernis      | Valkostur stilltur   |          | X          |
| Móðurmál                    | Leit       |          | X          |
| Fjöldi skjólstæðinga               | Heiltala |          |            |
| Uppgjafahermaður                     | Leit       |          | X          |
| Starfskraftur                             | Leit       | X        | X          |
| Númer persónuupplýsingar starfskrafts      | Text         | X        | X          |


**Bankareikningur starfskrafts**

| **Reitir**                 | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|----------------------------|---------------|--------------|----------------|
| Handhafi lykils             | Text          |              | X              |
| Kenni lykils     | Text          |              | X              |
| Aðseturslýsing        | Text          |              | X              |
| Gerð bankareiknings          | Valkostur stilltur    |              | X              |
| Staðsetning banka         | Text          |              | X              |
| Nafn útibús                | Text          |              | X              |
| Útibúsnúmer              | Text          |              | X              |
| Póststöð                       | Text          |              | X              |
| Land eða svæði          | Text          |              | X              |
| Sýsla                     | Text          |              | X              |
| Lýsing                | Text          |              | X              |
| Heiti svæðis              | Text          |              | X              |
| Netfang                      | Text          |              | X              |
| Skráarending                  | Text          |              | X              |
| Fax                        | Text          |              | X              |
| IBAN-númer                       | Text          |              | X              |
| Lína 1                     | Text          |              | X              |
| Lína 2                     | Text          |              | X              |
| Lína 3                     | Text          |              | X              |
| Farsími               | Text          |              | X              |
| Nafn             | Text          |              | X              |
| Póstnúmer                | Text          |              | X              |
| Póstkassi            | Text          |              |                |
| Leiðarnúmer             | Text          |              | X              |
| Gerð leiðarnúmers        | Valkostur stilltur    |              | X              |
| Fylki eða hérað          | Text          |              | X              |
| SWIFT kóði                 | Text          |              | X              |
| Sími                  | Text          |              | X              |
| Telexnúmer               | Text          |              | X              |
| Vefslóð                | Text          |              | X              |
| Starfskraftur                     | Leit        | X            | X              |
| Bankareikningsnúmer starfskrafts | Text          |              | X              |
| Bankareikningsnúmer starfskrafts | Text          | X            | X              |

**Föst laun starfskrafts**

| Reitir                                | Gagnagerð      | Krafa | Hægt að leita |
|---------------------------------------|----------------|----------|------------|
| Fyrirt.                                 | Leit         | X        | X          |
| Gerð styrks                     | Valkostur stilltur     |          | X          |
| Gjaldmiðill                              | Leit         |          | X          |
| Gildisdagsetning                        | Einungis dagsetning      |          | X          |
| Tilvik                                 | Leit         | X        | X          |
| Gengi                         | Fjöldi aukastafa |          | X          |
| Lokadagur                       | Einungis dagsetning      |          | X          |
| Línunúmer                           | Fjöldi aukastafa |          | X          |
| Greiðslutíðni                         | Leit         | X        | X          |
| Launataxti                              | Gjaldmiðill       |          | X          |
| Launataxti (grunnur)                       | Gjaldmiðill       |          | X          |
| Fyrirkomulag                                  | Leit         | X        | X          |
| Staða                              | Leit         | X        | X          |
| Gerð ferlis                          | Valkostur stilltur     | X        | X          |
| Uppsetningarlína tilvísunarpunkta            | Leit         |          | X          |
| Starfskraftur                                | Leit         | X        | X          |
| Númer fastra launa starfskrafts      | Text           | X        | X          |

**Kennitala starfskrafts**

| Reitir                 | Gagnagerð   | Krafa | Hægt að leita |
|------------------------|-------------|----------|------------|
| Lýsing            | Text        |          | X          |
| Gerð færslu             | Text        |          | X          |
| Lokadagur        | Einungis dagsetning   |          | X          |
| Auðkennisnúmer  | Text        | X        | X          |
| Gerð auðkennis    | Leit      | X        | X          |
| Er aðal             | Tveir möguleikar |          | X          |
| Útgáfudagur:             | Einungis dagsetning   |          | X          |
| Útgáfustofnun         | Leit      | X        | X          |
| Starfskraftur                 | Leit      | X        | X          |


## <a name="position-entities"></a>Stöðueiningar

**Staða starfs**

| **Reitir**               | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|--------------------------|----------------|--------------|----------------|
| Virkjun               | Dagsetning og tími  |              | X              |
| Tiltækt til úthlutunar | Dagsetning og tími  |              | X              |
| Deild               | Leit         |              | X              |
| Lýsing              | Text           |              | X              |
| Jafngildi fulls starfs     | Fjöldi aukastafa |              | X              |
| Vinnsla                      | Leit         | X            | X              |
| Númer starfsstöðu      | Text           | X            | X              |
| Staða yfirstarfs      | Leit         |              | X              |
| Gerð stöðu            | Leit         |              | X              |
| Starfslok               | Dagsetning og tími  |              | X              |
| Titill                    | Valkostur stilltur     |              | X              |
| Gildir frá               | Dagsetning og tími  | X            | X              |
| Gildir til                 | Dagsetning og tími  |              | X              |


**Tegund stöðu**

| **Reitir**         | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|--------------------|---------------|--------------|----------------|
| Flokkun     | Valkostur stilltur    |              | X              |
| Lýsing        | Text          |              | X              |
| Heiti stöðugerðar | Text          | X            | X              |


**Stöðuúthlutun starfskrafts**

| **Reitir**                        | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-----------------------------------|---------------|--------------|----------------|
| Staða starfs                      | Leit        | X            | X              |
| Stöðuúthlutunarnúmer starfskrafts | Text          | X            | X              |
| Gildir frá                        | Text          | X            | X              |
| Gildir til                          |               |              | X              |
| Starfskraftur                            |               | X            | X              |

## <a name="job-entities"></a>Starfseiningar

**Vinnsla**

| **Reitir**                   | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|------------------------------|----------------|--------------|----------------|
| Leyfa ótakmarkaðar stöður    | Tveir möguleikar    |              | X              |
| Sjálfgildi jafngildi fulls starfs | Fjöldi aukastafa |              | X              |
| Lýsing                  | Text           |              | X              |
| Starfslýsing              | Text           |              | X              |
| Starfshlutverk                 | Leit         |              | X              |
| Starfsgerð                     | Leit         |              | X              |
| Hámarksfjöldi staða  | Heiltala   |              | X              |
| Nafn                         | Text           | X            | X              |
| Titill                        | Valkostur stilltur     |              | X              |
| Gildir frá                   | Dagsetning og tími  | X            | X              |
| Gildir til                     | Dagsetning og tími  |              | X              |


**Starfshlutverk**

| **Reitir**        | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------------|---------------|--------------|----------------|
| Lýsing       | Text          | X            | X              |
| Heiti starfshlutverks | Text          | X            | X              |


**Vinnslugerð**

| **Reitir**    | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|---------------|---------------|--------------|----------------|
| Lýsing   | Text          | X            | X              |
| Undanþágustaða | Valkostur stilltur    | X            | X              |
| Heiti starfsgerðar | Text          | X            | X              |

## <a name="leave-and-absence-entities"></a>Einingar fyrir leyfi og fjarvistir

**Orlofsskráning**

| **Reitir**            | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-----------------------|---------------|--------------|----------------|
| Dagsetningagrunnur uppsöfnunar    | Einungis dagsetning     | X            | X              |
| Raunverulegur upphafsdagur    | Einungis dagsetning     | X            | X              |
| Sérstillt dagsetning           | Einungis dagsetning     | X            | X              |
| Er uppsöfnunarseinkað  | Tveir möguleikar   |              | X              |
| LeaveEnrollmentNumber | Text          | X            | X              |
| Leyfisáætlun            | Leit        | X            | X              |
| Upphafsdagsetning            | Einungis dagsetning     | X            | X              |
| Grunnur lags            | Valkostur stilltur    | X            | X              |
| Starfskraftur                | Leit        | X            | X              |


**Orlofsbankafærsla**

| **Reitir**                    | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|-------------------------------|----------------|--------------|----------------|
| Upphæð                        | Fjöldi aukastafa | X            | X              |
| Fyrirt.                         | Leit         | X            | X              |
| Bankafærslunúmer orlofs | Text           | X            | X              |
| Leyfisáætlun                    | Leit         |              | X              |
| Gerð leyfis                    | Leit         | X            | X              |
| Færsludagsetning              | Einungis dagsetning      | X            | X              |
| Færslunúmer            | Fjöldi aukastafa | X            | X              |
| Færslugerð              | Valkostur stilltur     | X            | X              |
| Starfskraftur                        | Leit         | X            | X              |


**Leyfisáætlun**

| **Reitir**        | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------------|---------------|--------------|----------------|
| Uppsöfnunartíðni | Valkostur stilltur    | X            | X              |
| Fyrirt.             | Leit        | X            | X              |
| Lýsing       | Text          |              | X              |
| Gerð leyfis        | Leit        | X            | X              |
| Nafn              | Text          | X            | X              |
| Upphafsdagsetning        | Einungis dagsetning     | X            | X              |


**Orlofsbeiðni**

| **Reitir**           | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|----------------------|---------------|--------------|----------------|
| Athugasemd              | Text          | X            | X              |
| Fyrirt.                | Leit        | X            | X              |
| Beiðninúmer orlofs | Text          |              | X              |
| Dagsetning beiðni         | Dagsetning og tími | X            | X              |
| Staða               | Valkostur stilltur    | X            | X              |
| Starfskraftur               | Leit        | X            | X              |


**Upplýsingar um orlofsbeiðni**

| **Reitir**                  | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|-----------------------------|----------------|--------------|----------------|
| Upphæð                      | Fjöldi aukastafa | X            | X              |
| Dagsetning leyfis                  | Dagsetning og tími  | X            | X              |
| Orlofsbeiðni               | Leit         | X            | X              |
| Upplýsinganúmer orlofsbeiðni | Text           | X            | X              |
| Gerð leyfis                  | Leit         | X            | X              |


**Gerð leyfis**

| **Reitir**      | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-----------------|---------------|--------------|----------------|
| Fyrirt.           | Leit        | X            | X              |
| Lýsing     | Text          |              | X              |
| Tekjukóði    | Leit        |              | X              |
| Heiti leyfisgerðar | Text          | X            | X              |


**Vinnudagatal**

| **Reitir**  | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------|---------------|--------------|----------------|
| Fyrirt.       | Leit        | X            | X              |
| Lýsing | Text          |              | X              |
| Nafn        | Text          | X            | X              |


**Dagur í vinnudagatali**

| **Reitir**               | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|--------------------------|---------------|--------------|----------------|
| Dagsetning dagatals            | Einungis dagsetning     | X            | X              |
| Fyrirt.                    | Leit        |              | X              |
| Staða                   | Text          |              | X              |
| Vinnudagatal            | Leit        | X            | X              |
| Númer dags í vinnudagatali | Text          | X            | X              |


**Frídagur í vinnudagatali**

| **Reitir**  | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------|---------------|--------------|----------------|
| Nafn        | Text          |              | X              |
| Lýsing | Text          | X            | X              |


**Frídagslína í vinnudagatali**

| **Reitir**                        | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-----------------------------------|---------------|--------------|----------------|
| Frídagur                      | Einungis dagsetning     | X            | X              |
| Nafn                              | Text          |              | X              |
| Frídagur í vinnudagatali             | Leit        | X            | X              |
| Frídagslínunúmer í vinnudagatali | Text          | X            | X              |


**Tímabil vinnudagatals**

| **Reitir**                         | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|------------------------------------|---------------|--------------|----------------|
| Fyrirt.                              | Leit        |              | X              |
| Lokatími                           | Heiltala  |              | X              |
| Upphafstími                         | Heiltala  |              | X              |
| Vinnudagatal                      | Leit        | X            | X              |
| Dagur í vinnudagatali                  | Leit        | X            | X              |
| Tímabilsnúmer vinnudagatals | Text          | X            | X              |

## <a name="organization-entities"></a>Fyrirtækjaeiningar

**Fyrirtæki**

| **Reitir**   | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|--------------|---------------|--------------|----------------|
| Fyrirtækiskóði | Text          | X            | X              |
| Nafn         | Text          | X            | X              |


**Deild**

| **Reitir**        | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------------|---------------|--------------|----------------|
| Deildarnúmer | Text          | X            | X              |
| Lýsing       | Text          |              | X              |
| Nafn              | Text          | X            | X              |
| Yfirdeild | Leit        |              | X              |


**Gjaldmiðill**

| **Reitir**         | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|--------------------|----------------|--------------|----------------|
| Gjaldmiðilskóði      | Text           | X            | X              |
| Heiti gjaldmiðils      | Text           | X            | X              |
| Gjaldmiðilsnákvæmni | Heiltala   | X            | X              |
| Gjaldmiðilstákn    | Text           | X            | X              |
| Einingamynd       | Mynd          |              |                |
| Gengi      | Fjöldi aukastafa | X            | X              |
| Stofnun/fyrirtæki       | Leit         | X            | X              |
| Staða             | Valkostur stilltur     |              | X              |

## <a name="payroll-entities"></a>Launaeiningar

**Greiðsluferli**

| **Reitir**  | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------|---------------|--------------|----------------|
| Lýsing | Text          | X            | X              |
| Tíðni   | Valkostur stilltur    | X            | X              |
| Nafn        | Text          | X            | X              |


**Launatímabil**

| **Reitir**           | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|----------------------|---------------|--------------|----------------|
| Sjálfgefin dagsetning greiðslu | Einungis dagsetning     |              | X              |
| Lýsing          | Text          |              | X              |
| Greiðsluferli            | Horfa          | X            | X              |
| Launatímabilsnúmer    | Text          | X            | X              |
| Lokadagsetning tímabils      | Einungis dagsetning     | X            | X              |
| Upphafsdagsetning tímabils    | Einungis dagsetning     | X            | X              |
| Staða               | Valkostur stilltur    |              | X              |


**Tekjukóði launa**

| **Reitir**              | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------------------|---------------|--------------|----------------|
| Lýsing             | Text          | X            | X              |
| Taka með í keyrslugerð greiðslu | Valkostur stilltur    | X            | X              |
| Er framleiðni           | Tveir möguleikar   | X            | X              |
| Nafn                    | Text          |              | X              |
| Magneining           | Valkostur stilltur    |              | X              |
| Rekja FMLA tíma        | Tveir möguleikar   |              | X              |


**Skattumdæmi**

| **Reitir**        | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------------|---------------|--------------|----------------|
| Póststöð              | Text          |              | X              |
| Land eða svæði | Text          |              | X              |
| Sýsla            | Text          |              | X              |
| Nafn              | Text          | X            | X              |
| Fylki eða hérað | Text          |              | X              |


**Útreikningsíðni fríðinda á launatímabili**

| **Reitir**                                      | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-------------------------------------------------|---------------|--------------|----------------|
| Útreikningstíðni fríðinda                   | Leit        | X            | X              |
| Útreikningsíðninúmer fríðinda á launatímabili | Text          | X            | X              |
| Launatímabil                                      | Leit        | X            | X              |


**Bankareikningsgreiðslur**

| **Reitir**                       | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|----------------------------------|----------------|--------------|----------------|
| Upphæð                           | Gjaldmiðill       |              | X              |
| Upphæð (grunnur)                    | Gjaldmiðill       |              | X              |
| Bankareikningur                     | Leit         | X            | X              |
| Númer bankareikningsgreiðslu | Text           | X            | X              |
| Fyrirt.                            | Leit         | X            | X              |
| Gjaldmiðill                         | Leit         |              | X              |
| Gengi                    | Fjöldi aukastafa |              | X              |
| Er eftirstöðvar                     | Tveir möguleikar    |              | X              |
| Forgangur                         | Heiltala   |              | X              |

**Útgáfustofnun persónuskilríkja**

| **Reitir**           | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|----------------------|---------------|--------------|----------------|
| Aðseturslýsing  | Text          |              | X              |
| Heimilisfang, lína 1       | Text          |              | X              |
| Heimilisfang, lína 2       | Text          |              | X              |
| Heimilisfang, lína 3       | Text          |              | X              |
| Póststöð                 | Text          |              | X              |
| Land eða svæði    | Valkostur stilltur    |              | X              |
| Sýsla               | Text          |              | X              |
| Lýsing          | Text          |              | X              |
| Netfang                | Text          |              | X              |
| Skráarending            | Text          |              | X              |
| Fax                  | Text          |              | X              |
| Heiti útgáfustofnunar  | Text          | X            | X              |
| Farsími         | Text          |              | X              |
| Síða                 | Text          |              | X              |
| Póstnúmer          | Text          |              | X              |
| Póstkassi      | Text          |              | X              |
| SMS                  | Text          |              | X              |
| Fylki eða hérað    | Text          |              | X              |
| Sími            | Text          |              | X              |
| Telex                | Text          |              | X              |
| Vefslóð          | Text          |              | X              |

**Persónukennisgerð starfskrafts**

| **Reitir**                        | **Gagnagerð**  | **Áskilið** | **Hægt að leita** |
|-----------------------------------|----------------|--------------|----------------|
| Heimiluð gildi                    | Valkostur stilltur     |              | X              |
| Land eða svæði                 | Text           |              | X              |
| Lýsing                       | Text           |              | X              |
| Föst lengd                      | Heiltala   |              | X              |
| Snið auðkennis      | Text           |              | X              |
| Gerð                              | Valkostur stilltur     |              | X              |
| Persónukennisgerð starfskrafts | Text           | X            | X              |

## <a name="fixed-compensation-entities"></a>Einingar fastra launa

**Fyrirkomulag fastra launa**

| **Reitir**                  | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-----------------------------|---------------|--------------|----------------|
| Fyrirt.                       | Leit        | X            | X              |
| Launanet           | Leit        |              | X              |
| Gjaldmiðill                    | Leit        | X            | X              |
| Lýsing                 | Text          | X            | X              |
| Gildisdagsetning              | Einungis dagsetning     | X            | X              |
| Lokadagur             | Einungis dagsetning     | X            | X              |
| Ráðningarregla                   | Valkostur stilltur    | X            | X              |
| Nafn                        | Text          | X            | X              |
| Leyfileg 'út fyrir svæðið' mörk      | Valkostur stilltur    | X            | X              |
| Greiðslutíðni               | Leit        | X            | X              |
| Leyfðar ráðleggingar      | Tveir möguleikar   | X            | X              |
| Uppsetning tilvísunarpunkta  | Leit        |              | X              |
| Gerð                        | Valkostur stilltur    | X            | X              |

**Launanet**

| **Reitir**                  | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-----------------------------|---------------|--------------|----------------|
| Fyrirt.                       | Leit        | X            | X              |
| Gjaldmiðill                    | Leit        |              | X              |
| Lýsing                 | Text          | X            | X              |
| Gildisdagsetning              | Einungis dagsetning     |              | X              |
| Lokadagur             | Einungis dagsetning     |              | X              |
| Nafn                        | Text          | X            | X              |
| Uppsetning tilvísunarpunkta       | Leit        | X            | X              |
| Gerð                        | Valkostur stilltur    | X            | X              |

**Launastig**

| **Reitir**      | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-----------------|---------------|--------------|----------------|
| Lýsing     | Text          |              | X              |
| Nafn            | Text          | X            | X              |
| Gerð            | Valkostur stilltur     | X            | X              |

**Greiðslutíðni launa**

| **Reitir**                  | **Gagnagerð**   | **Áskilið** | **Hægt að leita** |
|-----------------------------|-----------------|--------------|----------------|
| Árlegur umreiknistuðull    | Fjöldi aukastafa  |              | X              |
| Fyrirt.                       | Leit          | X            | X              |
| Lýsing                 | Text            |              | X              |
| Umreiknistuðull samkvæmt tímafjölda    | Fjöldi aukastafa  |              | X              |
| Mánaðarlegur umreiknistuðull   | Fjöldi aukastafa  |              | X              |
| Nafn                        | Text            | X            | X              |
| Tímabil                      | Valkostur stilltur      |              | X              |
| Vikulegur umreiknistuðull    | Valkostur stilltur      |              | X              |


**Uppsetning á tilvísunarpunkti launa**

| **Reitir**          | **Gagnagerð**   | **Áskilið** | **Hægt að leita** |
|---------------------|-----------------|--------------|----------------|
| Fyrirt.               | Leit          | X            | X              |
| Gerð styrks   | Valkostur stilltur      | X            | X              |
| Lýsing         | Text            | X            | X              |
| Nafn                | Text            | X            | X              |

**Setja upp línu tilvísunarpunkts launa**

| **Reitir**            | **Gagnagerð**   | **Áskilið** | **Hægt að leita** |
|-----------------------|-----------------|--------------|----------------|
| Fyrirt.                 | Leit          | X            | X              |
| Lýsing           | Text            | X            | X              |
| Línunúmer           | Fjöldi aukastafa  | X            | X              |
| Nafn                  | Text            | X            | X              |
| Uppsetning tilvísunarpunkta | Leit          | X            | X              |

**Launasvæði**

| **Reitir**      | **Gagnagerð** | **Áskilið** | **Hægt að leita** |
|-----------------|---------------|--------------|----------------|
| Lýsing     | Text          | X            | X              |
| Nafn            | Text          | X            | X              |

**Launaskipulag**

| **Reitir**                    | **Gagnagerð**   | **Áskilið** | **Hægt að leita** |
|-------------------------------|---------------  |--------------|----------------|
| Upphæð                        | Gjaldmiðill        |              | X              |
| Upphæðargrunnur                   | Gjaldmiðill        |              | X              |
| Fyrirt.                         | Leit          | X            | X              |
| Númer launaskipulags | Text            | X            | X              |
| Gjaldmiðill                      | Leit          |              | X              |
| Gengi                 | Fjöldi aukastafa  |              | X              |
| Hnitanet                          | Leit          | X            | X              |
| Stig                         | Leit          | X            | X              |
| Tilvísunarpunktur               | Leit          | X            | X              |
| Uppsetning tilvísunarpunkta    | Leit          | X            | X              |

**Fast launatilvik**

| **Reitir**            | **Gagnagerð**   | **Áskilið** | **Hægt að leita** |
|-----------------------|-----------------|--------------|----------------|
| Fyrirt.                 | Leit          | X            | X              |
| Lýsing           | Text            | X            | X              |
| Gerð tilviks            | Valkostur stilltur      | X            | X              |
| Er virkt             | Tveir möguleikar     | X            |                |
| Nafn                  | Text            | X            | X              |

## <a name="entity-relationship-models"></a>Einingaþáttur tengslalíkanseiningar

### <a name="worker"></a>Starfskraftur
![Starfskraftur](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Starf og starfstaða
![Starf og starfstaða](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Fríðindi
![Fríðindi](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Laun
![Laun](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Hætta
![Hætta](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Vinnudagatal
![Vinnudagatal](./media/HCMCommon-work-calendar-entity-diagram.png)
