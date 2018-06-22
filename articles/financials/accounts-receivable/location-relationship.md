---
title: "Bæta við tengslagerðum staðsetningar og aðila"
description: "Þetta efnisatriði útskýrir hvernig á að bæta við nýjum tengslagerðum fyrir staðsetningar og aðila."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: bd8c5a18d69e1952d32675d759b8b2a997844822
ms.contentlocale: is-is
ms.lasthandoff: 05/21/2018

---

# <a name="add-new-location-roles-and-party-relationship-types"></a>Bættu við nýjum tegnslagerðum fyrir hlutverk staðsetningar og aðila 

## <a name="add-new-location-roles"></a>Bæta við nýjum staðsetningarhlutverkum

Það eru tvær leiðir til að bæta við nýjum staðsetningarhlutverkum fyrir aðsetur og tengslaupplýsingar:

-  Bæta þeim við í gegnum síðuna **Málefni aðseturs og tengslaupplýsinga**. Nýja hlutverkið verður vistað í töflunni **LogisticsLocationRole** með gerðinni = 0, sem gefur til kynna að hlutverkið sé ekki kerfishlutverk sem er skilgreint í fasttextanum **LogisticsLocationRoleType** og viðbótum hans. Notandi getur notað þetta hlutverk þegar hann býr til aðseturs- eða tengslaupplýsingar.

    ![Málefni aðseturs- og innihaldsupplýsinga](media/Address-Contact.PNG)

-  Bæta þeim við viðbót fasttextans **LogisticsLocationRoleType** og leyfa útfyllingu í gegnum f fylla í gegnum samstillingarferli gagnagrunns.

    1.  Búa til viðbót við fasttextann **LogisticsLocationRoleType** og bæta nýja hlutverkinu við viðbótina. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Búa til nýja tilfangaskrá fyrir nýja hlutverkið og úthluta síðan gildi fyrir eiginleika hennar.
     
     ![Ný tilfangaskrá](media/Resource.PNG)
        
    3.  Búa til fyllingaklasa fyrir gögn og útvega rekilaðferð til að fylla út í nýja hlutverkið. 

        ![Gagnafylling](media/Dirdata.PNG)

    4.  Til að prófa að fylla nýja staðsetningarhlutverkið geturðu búið til keyranlegan klasa og kallað í DirDataPopulation::insertLogisticsLocationRoles() í Main(). Eftir að þessu ferli er lokið ættir þú að sjá nýja hlutverkið sem er fyllt út í töflunni **LogisticsLocationRole** með gerðinni \> 0. Nýja hlutverkið mun birtast á síðunni **Málefni aðseturs- og tengslaupplýsinga**.

        ![Setja inn nýja staðsetningu](media/InsertNewLocation.PNG)

## <a name="add-new-party-relationship-types"></a>Bæta við nýrri tengslagerð aðila 

Það eru tvær leiðir til að bæta við nýrri tengslagerð:

-   Bæta henni við í gegnum síðuna **Tengslagerðir**. Nýju tengslin verða vistuð í **DirRelationshipTypeTable** með systemtype = 0.

    ![Gerðir tengsla](media/Relationship.PNG)

-  Bæta þeim við viðbót fasttextans **DirSystemRelationshipType** og láta þeim að fylla í gegnum samstillingarferli gagnagrunns.

    1.  Búa til viðbót við fasttextann **DirSystemRelationshipType** og bæta við nýju tengslagerðinni.

    2. Stofna frumstillingu fyrir þessa nýja gerð. Þú getur fundið nokkur dæmi í kjarnakóðanum, einn þeirra er **DirRelationshipTypeChildInitialize**. Þetta er frumstillingarklasi fyrir aðilatengslagerðina "undireining". Þú getur byrjað með frumstillinguna þína með því að afrita og líma þennan kóða og uppfæra síðan merktu svæðin.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Til að prófa að fylla nýju tengslagerðina er hægt að stofna keyranlegan klasa og kalla í DirDataPopulation::insertDirRelationshipTypes() í Main(). Þú ættir að sjá nýju tengslagerðina í **DirRelationshipTypeTable** og nýja tengslagerðin verður aðgengileg á síðunni **Tengslagerðir**.

        ![Keyranlegur klasi](media/Runnable.PNG)

