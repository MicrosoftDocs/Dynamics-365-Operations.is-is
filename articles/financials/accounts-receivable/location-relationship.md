---
title: Bæta við tengslagerðum staðsetningar og aðila
description: Þetta efnisatriði útskýrir hvernig á að bæta við nýjum tengslagerðum fyrir staðsetningar og aðila.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 543784e8072f88c10f63e1b44921b9f2d37308c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549699"
---
# <a name="add-location-roles-and-party-relationship-types"></a><span data-ttu-id="f2ff6-103">Bæta við staðsetningarhlutverkum og aðilatengslagerðum</span><span class="sxs-lookup"><span data-stu-id="f2ff6-103">Add location roles and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="f2ff6-104">Bæta við staðsetningarhlutverkum</span><span class="sxs-lookup"><span data-stu-id="f2ff6-104">Add location roles</span></span>

<span data-ttu-id="f2ff6-105">Það eru tvær leiðir til að bæta við nýjum staðsetningarhlutverkum fyrir aðsetur og tengslaupplýsingar:</span><span class="sxs-lookup"><span data-stu-id="f2ff6-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="f2ff6-106">Bæta þeim við í gegnum síðuna **Málefni aðseturs og tengslaupplýsinga**.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="f2ff6-107">Nýja hlutverkið verður vistað í töflunni **LogisticsLocationRole** með gerðinni = 0, sem gefur til kynna að hlutverkið sé ekki kerfishlutverk sem er skilgreint í fasttextanum **LogisticsLocationRoleType** og viðbótum hans.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="f2ff6-108">Notandi getur notað þetta hlutverk þegar hann býr til aðseturs- eða tengslaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Málefni aðseturs- og innihaldsupplýsinga](media/Address-Contact.PNG)

-  <span data-ttu-id="f2ff6-110">Bæta þeim við viðbót fasttextans **LogisticsLocationRoleType** og leyfa útfyllingu í gegnum f fylla í gegnum samstillingarferli gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="f2ff6-111">Búa til viðbót við fasttextann **LogisticsLocationRoleType** og bæta nýja hlutverkinu við viðbótina.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="f2ff6-113">Búa til nýja tilfangaskrá fyrir nýja hlutverkið og úthluta síðan gildi fyrir eiginleika hennar.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Ný tilfangaskrá](media/Resource.PNG)
        
    3.  <span data-ttu-id="f2ff6-115">Búa til fyllingaklasa fyrir gögn og útvega rekilaðferð til að fylla út í nýja hlutverkið.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Gagnafylling](media/Dirdata.PNG)

    4.  <span data-ttu-id="f2ff6-117">Til að prófa að fylla nýja staðsetningarhlutverkið geturðu búið til keyranlegan klasa og kallað í DirDataPopulation::insertLogisticsLocationRoles() in Main().</span><span class="sxs-lookup"><span data-stu-id="f2ff6-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="f2ff6-118">Eftir að þessu ferli er lokið ættir þú að sjá nýja hlutverkið sem er fyllt út í töflunni **LogisticsLocationRole** með gerðinni \> 0.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="f2ff6-119">Nýja hlutverkið mun birtast á síðunni **Málefni aðseturs- og tengslaupplýsinga**.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Setja inn nýja staðsetningu](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="f2ff6-121">Bæta við aðilatengslagerðum</span><span class="sxs-lookup"><span data-stu-id="f2ff6-121">Add party relationship types</span></span> 

<span data-ttu-id="f2ff6-122">Það eru tvær leiðir til að bæta við nýrri tengslagerð:</span><span class="sxs-lookup"><span data-stu-id="f2ff6-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="f2ff6-123">Bæta henni við í gegnum síðuna **Tengslagerðir**.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="f2ff6-124">Nýju tengslin verða vistuð í **DirRelationshipTypeTable** með systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Gerðir tengsla](media/Relationship.PNG)

-  <span data-ttu-id="f2ff6-126">Bæta þeim við viðbót fasttextans **DirSystemRelationshipType** og láta þeim að fylla í gegnum samstillingarferli gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="f2ff6-127">Búa til viðbót við fasttextann **DirSystemRelationshipType** og bæta við nýju tengslagerðinni.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="f2ff6-128">Stofna frumstillingu fyrir þessa nýja gerð.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-128">Create an initializer for this new type.</span></span> <span data-ttu-id="f2ff6-129">Þú getur fundið nokkur dæmi í kjarnakóðanum, einn þeirra er **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="f2ff6-130">Þetta er frumstillingarklasi fyrir aðilatengslagerðina "undireining".</span><span class="sxs-lookup"><span data-stu-id="f2ff6-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="f2ff6-131">Þú getur byrjað með frumstillinguna þína með því að afrita og líma þennan kóða og uppfæra síðan merktu svæðin.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="f2ff6-133">Til að prófa að fylla nýju tengslagerðina er hægt að stofna keyranlegan klasa og kalla í DirDataPopulation::insertDirRelationshipTypes() in Main().</span><span class="sxs-lookup"><span data-stu-id="f2ff6-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="f2ff6-134">Þú ættir að sjá nýju tengslagerðina í **DirRelationshipTypeTable** og nýja tengslagerðin verður aðgengileg á síðunni **Tengslagerðir**.</span><span class="sxs-lookup"><span data-stu-id="f2ff6-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Keyranlegur klasi](media/Runnable.PNG)
