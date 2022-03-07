---
title: Formúluhönnuður fyrir TDS-útreikninga
description: Þetta efnisatriði er dæmi um hvernig skattur sem er dreginn er frá í uppruna (TDS) er reiknaður á grundvelli formúlunnar sem er skilgreind fyrir hvern TDS-skattkóða í TDS-hópnum sem er tengdur færslunni.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e9c97982233b1f3dc3924fa42954b5cb8d09ffcaa07d19a3892b25737a6c29c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778870"
---
# <a name="formula-designer-for-tds-calculations"></a>Formúluhönnuður fyrir TDS-útreikninga

[!include [banner](../includes/banner.md)]

Þetta efnisatriði er dæmi um hvernig skattur sem er dreginn er frá í uppruna (TDS) er reiknaður á grundvelli formúlunnar sem er skilgreind fyrir hvern TDS-skattkóða. TDS-skattkóðar eru skilgreindir í TDS-hópnum sem er tengdur færslunni. Ljúkið við grunnuppsetninguna sem þarf fyrir TDS eins og lýst er í eftirfarandi skrefum áður en TDS formúlurnar eru hannaðar. 

- Setja upp TDS hlutahópa með því að nota síðuna **Íhlutaflokkar staðgreiðsluskatts**. 
- Settu upp TDS íhluti og festu TDS íhlutahópinn við TDS íhlutina með því að nota síðuna **Staðgreiðsluskattshlutar**. 
- Setjið upp skattkóða TDS og hengið TDS-hluta við skattkóðana með síðunni **Staðgreiðsluskattskóðar**. 
- Setjið upp flokka TDS-skatts á síðunni **Staðgreiðsluskattsflokkar**. Tengdu svo TDS skattkóðana við skattflokkinn og skilgreindu formúluna með því að nota síðun **Formúluhönnuður**. 

**Dæmi um formúlu**

Í þessu dæmi er TDS-hópurinn, Leiga, hengdur við innkaupareikning sem er búinn til fyrir söluaðila A. Reikningsupphæðin er USD 100.000. Vísað er til eftirfarandi töflu til að skoða TDS-útreikninginn fyrir reikninginn.

| TDS hópur                                                   | TDS-skattkóði sem er hengdur við TDS-flokkinn | Virði              | Skattskyldur grunnur (formúluhönnuður) | Segð útreiknings (Formúluhönnuður) | Grunnupphæð | Reiknuð TDS-upphæð |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Leiga                                                         | TDS  (TDS íhlutur - TDS)                | 10%                | Brúttó upphæð                      |                                            | 100,000      | 10,000                 |
| Viðbótargjald  (TDS-hluti - Viðbótargjald)                         | 10%                                     | Án brúttóupphæðar | +TDS                              |                   10000                    | 1.000        |                       |
| PE-Cess  (TDS-hluti - PE-Cess)                            | 2%                                      | Án brúttóupphæðar | +TDS+Aukagjald                    |                   11000                    | 220         |                       |
| SHE Cess  (TDS hluti- SHE Cess)                          | 1%                                      | Án brúttóupphæðar | +TDS+Aukagjald                    |                   11000                    | 110         |                       |
| **Alls** **TDS**  **reiknaður** **fyrir** **** **reikninginn** | **11,330**                               |                    |                                   |                                            |             |                       |

Fylgiskjalsfærslurnar eru stofnaðar á eftirfarandi hátt.

| Lykill           | Debet  | Kredit |
| ----------------- | ------ | ------ |
| Leiga              | 100,000 |        |
| Lánardrottinn A          |        | 100,000 |
| Lánardrottinn A          | 11,330  |        |
| TDS til greiðslu       |        | 10,000  |
| Aukagjald til greiðslu |        | 1.000   |
| PE-Cess til greiðslu   |        | 220    |
| SHE Cess til greiðslu  |        | 110    |
