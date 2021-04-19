---
title: Kostnaður viðhaldsáætlunar
description: Þetta efni skýrir kostnað viðhaldsskema í eignastýringu.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 405fd7fbbbb8862446d09b9ea33ef14348e691f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813774"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="990bb-103">Kostnaður viðhaldsáætlunar</span><span class="sxs-lookup"><span data-stu-id="990bb-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="990bb-104">Í eignastjórnun geturðu reiknað út kostnaðaráætlun á viðhaldsskemalínum.</span><span class="sxs-lookup"><span data-stu-id="990bb-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="990bb-105">Þetta er gagnlegt ef þú vilt fá yfirsýn yfir væntanlegan kostnað, til dæmis kostnað vegna fyrirhugaðra forvirkra viðhaldsverka næsta árið.</span><span class="sxs-lookup"><span data-stu-id="990bb-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="990bb-106">Útreikningarnir eru byggðir á núverandi viðhaldsskemalínum af gerðinni „Viðhaldsáætlanir“ og „Viðhaldslotur“ og „Viðhaldsbeiðnir“.</span><span class="sxs-lookup"><span data-stu-id="990bb-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="990bb-107">Smelltu á **Eignastýring** > **Fyrirspurnir** > **Eignir** > **Kostnaður við viðhaldsskema**.</span><span class="sxs-lookup"><span data-stu-id="990bb-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="990bb-108">Í valmyndinni **Kostnaður við viðhaldsskema** er hægt að velja **Fjárhagsvídd stillt** ef þú vilt sjá kostnað flokkaðan í fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="990bb-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="990bb-109">Fjárhagsvíddarsett eru sett upp í **Fjárhag** > **Bókhaldslykli** > **Víddir** > **Fjárhagsvíddarsett**.</span><span class="sxs-lookup"><span data-stu-id="990bb-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="990bb-110">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að viðhaldsskemalínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="990bb-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="990bb-111">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar viðhaldsskemalínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="990bb-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="990bb-112">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar viðhaldsskemalínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="990bb-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="990bb-113">Ef þú vilt gera útreikning á tilteknum eignum skaltu smella á **Sía** á flýtiflipanum **Færslur til að hafa með** og velja viðeigandi eignir.</span><span class="sxs-lookup"><span data-stu-id="990bb-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="990bb-114">Ef þess er krafist geturðu einnig tilgreint dagsetningu **Væntanlegt upphaf** fyrir kostnaðarútreikning eða valið aðra **Stöðu** fyrir kostnaðarútreikninginn</span><span class="sxs-lookup"><span data-stu-id="990bb-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="990bb-115">Smellið á **Í lagi** til að hefja kostnaðarútreikning.</span><span class="sxs-lookup"><span data-stu-id="990bb-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="990bb-116">Á flipanum **Kostnaður viðhaldsáætlunar** > í **Flokka eftir...** aðgerðarsvæðishópum skal smella á viðeigandi hnappa til að sýna nauðsynlegt upplýsingastig kostnaðarútreikningsins.</span><span class="sxs-lookup"><span data-stu-id="990bb-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="990bb-117">Hnappar valinna aðgerðasvæðahóps eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="990bb-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="990bb-118">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="990bb-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="990bb-119">Smelltu á hnappinn **Reikna kostnað** ef þú vilt gera nýjan kostnaðarútreikning.</span><span class="sxs-lookup"><span data-stu-id="990bb-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="990bb-120">Myndin hér að neðan sýnir niðurstöður útreiknings á kostnaði viðhaldsskema.</span><span class="sxs-lookup"><span data-stu-id="990bb-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Mynd 1](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]