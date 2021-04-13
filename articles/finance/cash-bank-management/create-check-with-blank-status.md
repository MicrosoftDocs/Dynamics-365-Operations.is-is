---
title: Búa til auðar ávísanir
description: Þetta efnisatriði útskýrir hvernig á að búa til auðar ávísanir fyrir bankareikning á síðunni Ávísanir.
author: abruer
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1b01daa86055156092d035d61aad78a13349f869
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815957"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="85736-103">Búa til auðar ávísanir</span><span class="sxs-lookup"><span data-stu-id="85736-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85736-104">Þetta efnisatriði útskýrir hvernig á að búa til auðar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="85736-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="85736-105">Til dæmis væri hægt að stofna auða ávísun til að skrá ávísun sem hefur skemmst og er ekki hægt að nota til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="85736-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="85736-106">Á síðunni **Ávísanir** er hægt að framkvæma viðhaldsverk fyrir ávísanir.</span><span class="sxs-lookup"><span data-stu-id="85736-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="85736-107">Til dæmis er hægt að búa til ný ávísunarnúmer og eyða ávísunum.</span><span class="sxs-lookup"><span data-stu-id="85736-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="85736-108">Einnig er hægt að búa til ávísanir með stöðuna **Auð**.</span><span class="sxs-lookup"><span data-stu-id="85736-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="85736-109">Eftir að auðar ávísanir eru stofnaðar er ekki hægt að eyða þeim eða endurnýta þær í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="85736-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="85736-110">Þessi eiginleiki er aðeins í boði á síðunni **Ávísanir** og aðeins ef kveikt er á eiginleikanum **Búa til auðar ávísanir á ávísanasíðunni** á síðunni **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="85736-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="85736-111">Ef ekki er kveikt er á eiginleikanum er einungis hægt að stofna **auðar** ávísanir í svarglugganum **Greiðsla með ávísun** meðan á greiðslumyndun stendur í viðskiptaskuldum.</span><span class="sxs-lookup"><span data-stu-id="85736-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="85736-112">Til að opna síðuna **Ávísanir** skal fara í **Reiðufjár-og bankastjórnun \> Bankareikningar \> Bankareikningar** og síðan, á aðgerðasvæðinu. í flipann **Stjórna greiðslum** í hópnum **Tengdar upplýsingar** og velja **Ávísanir**.</span><span class="sxs-lookup"><span data-stu-id="85736-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="85736-113">Einnig er hægt að fara í **Reiðufjár- og bankastjórnun \> Fyrirspurnir og skýrslur \> Ávísanir**.</span><span class="sxs-lookup"><span data-stu-id="85736-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="85736-114">Síðan, til að búa til ávísanir með stöðuna **Auð** á aðgerðasvæðinu, skal velja **Stofna auðar ávísanir**.</span><span class="sxs-lookup"><span data-stu-id="85736-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="85736-115">Þegar kerfið er að búa til auðar ávísanir er tengdur bankareikningur gerður óvirkur tímabundið.</span><span class="sxs-lookup"><span data-stu-id="85736-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="85736-116">Þessi virkni dregur úr hættunni á því að greiðslur verði myndaðar á sama tíma og auðar ávísanir eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="85736-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="85736-117">Þegar vinnslunni er lokið er tengdur bankareikningur endurvirkjaður.</span><span class="sxs-lookup"><span data-stu-id="85736-117">When the processing is completed, the associated bank account is reactivated.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]