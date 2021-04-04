---
title: Samþætting athugasemdar
description: Í þessu efnisatriði er lýst samþættingu athugasemdagagna í tvöfaldri skráningu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 221be52b4d66aaa47f9a1919d5d0b9f8459b7ff9
ms.sourcegitcommit: db9b35ce6968cad8874b3c13d4c02d84e2617c8b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/11/2021
ms.locfileid: "5577607"
---
# <a name="note-integration"></a><span data-ttu-id="87320-103">Samþætting athugasemdar</span><span class="sxs-lookup"><span data-stu-id="87320-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="87320-104">Í viðskiptaferlum safna notendur Microsoft Dynamics 365 oft saman upplýsingum um viðskiptavini sína.</span><span class="sxs-lookup"><span data-stu-id="87320-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="87320-105">Þessar upplýsingar eru skráðar sem verkþættir og athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="87320-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="87320-106">Í þessu efnisatriði er lýst samþættingu athugasemdagagna í tvöfaldri skráningu.</span><span class="sxs-lookup"><span data-stu-id="87320-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="87320-107">Hægt er að flokka upplýsingar um viðskiptavin á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="87320-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="87320-108">**Aðgerðartengdar upplýsingar sem notandi Dynamics 365 framkvæmir fyrir hönd viðskiptavinar** – Til dæmis Contoso (notandi Dynamics 365) er að stjórna spurningakeppni.</span><span class="sxs-lookup"><span data-stu-id="87320-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="87320-109">Einn af viðskiptavinum Contoso (viðskiptavinur) vill mæta á spurningakeppnina.</span><span class="sxs-lookup"><span data-stu-id="87320-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="87320-110">Viðskiptavinurinn biður starfsmann Contoso að bóka pláss fyrir sig í spurningakeppninni.</span><span class="sxs-lookup"><span data-stu-id="87320-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="87320-111">Bókunin á sér stað í dagatali þátttakanda fyrir viðburð Contoso.</span><span class="sxs-lookup"><span data-stu-id="87320-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="87320-112">**Aðgerðartengdar upplýsingar fyrir notanda Dynamics 365** – Til dæmis færir viðskiptavinur sem er að kaupa Surface-tölvu inn sérstakar upplýsingar sem gefa til kynna að pakka eigi tækinu inn í gjafapappír fyrir afhendingu.</span><span class="sxs-lookup"><span data-stu-id="87320-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="87320-113">Þessar leiðbeiningar eru aðgerðartengdar upplýsingar sem starfsmaður Contoso, sem er ábyrgur fyrir pökkun, á að sjá um.</span><span class="sxs-lookup"><span data-stu-id="87320-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="87320-114">**Upplýsingar sem tengjast ekki aðgerð** – Til dæmis heimsækir viðskiptavinur verslun Contoso og í samtali við starfsmann verslunarinnar segist hann hafa áhuga á *Halo-leikjum* og aukabúnaði tölvuleikja.</span><span class="sxs-lookup"><span data-stu-id="87320-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="87320-115">Starfsmaður verslunarinnar skrifar athugasemd varðandi þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="87320-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="87320-116">Tillöguvél afurða notar hana þá til að senda viðskiptavini tillögur.</span><span class="sxs-lookup"><span data-stu-id="87320-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="87320-117">Almennt eru aðgerðartengdar upplýsingar sóttar sem *verkþættir* í Finance and Operations-forritum og forritum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="87320-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="87320-118">Upplýsingar sem tengjast ekki aðgerð eru sóttar sem *athugasemdir* í Finance and Operations-forritum og sem *skýringar* í forritum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="87320-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="87320-119">Þótt athugasemdir séu ætlaðar fyrir upplýsingar sem tengjast ekki aðgerð munu forritin ekki koma í veg fyrir að þær séu notaðar til að geyma og meðhöndla aðgerðartengdar upplýsingar ef ætlunin er að nota þær í þeim tilgangi.</span><span class="sxs-lookup"><span data-stu-id="87320-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="87320-120">Microsoft er að gefa út virkni fyrir samþættingu athugasemda.</span><span class="sxs-lookup"><span data-stu-id="87320-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="87320-121">(Virkni fyrir samþættingu verkþáttar verður gefin út síðar.) Samþætting athugasemdar er í boði fyrir viðskiptavini, lánardrottna, sölupantanir og innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="87320-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="87320-122">Búa til athugasemd í forriti viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="87320-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="87320-123">Til að búa til athugasemd í forriti viðskiptavinar og því næst samstilla hana við Finance and Operations-forrit skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="87320-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="87320-124">Í forriti viðskiptavinar skal opna reikningsfærslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87320-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="87320-125">Á svæðinu **Tímalína** skal velja plúsmerkið (**+**) og síðan velja **Athugasemd** til að búa til athugasemd.</span><span class="sxs-lookup"><span data-stu-id="87320-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Athugasemd búin til í forriti viðskiptavinar](media/notes-ce-1.png)

3. <span data-ttu-id="87320-127">Færið inn titil og lýsingu og veljið síðan **Bæta við athugasemd**.</span><span class="sxs-lookup"><span data-stu-id="87320-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Titill og lýsing færð inn](media/notes-ce-2.png)

    <span data-ttu-id="87320-129">Nýja athugasemdin bætist við tímalínu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87320-129">The new note is added to the customer timeline.</span></span>

    ![Ný athugasemd á tímalínu viðskiptavinar](media/notes-ce-3.png)

4. <span data-ttu-id="87320-131">Skráið ykkur inn í Finance and Operations-forritið og opnið sömu viðskiptavinafærsluna.</span><span class="sxs-lookup"><span data-stu-id="87320-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="87320-132">Takið eftir að hnappurinn **Viðhengi** (bréfaklemmutákn) efst í hægra horninu gefur til kynna að færslan sé með viðhengi.</span><span class="sxs-lookup"><span data-stu-id="87320-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Tilkynning um viðhengi](media/notes-ce-4.png)

5. <span data-ttu-id="87320-134">Veljið hnappinn **Viðhengi** til að opna síðuna **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="87320-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="87320-135">Athugasemdin sem var búin til ætti að finnast í forriti viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87320-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Athugasemd úr forriti viðskiptavinar](media/notes-ce-5.png)

<span data-ttu-id="87320-137">Allar uppfærslur á athugasemdinni eru samstilltar fram og til baka milli Finance and Operations-forritsins og forrits viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87320-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="87320-138">Búa til athugasemd í Finance and Operations forriti</span><span class="sxs-lookup"><span data-stu-id="87320-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="87320-139">Einnig er hægt að búa til athugasemd í Finance and Operations-forriti og verður hún samstillt við forrit viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87320-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="87320-140">Til að búa til athugasemd í Finance and Operations-forriti og því næst samstilla hana við forrit viðskiptavinar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="87320-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="87320-141">Í Finance and Operations-forritinu, á síðunni **Viðhengi**, skal velja **Ný** \> **Athugasemd**.</span><span class="sxs-lookup"><span data-stu-id="87320-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Athugasemd búin til í Finance and Operations-forritinu](media/notes-fo-1.png)

2. <span data-ttu-id="87320-143">Færið inn titil og leiðbeiningar í stuttu máli og veljið síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="87320-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Titill og leiðbeiningar færðar inn](media/notes-fo-2.png)

3. <span data-ttu-id="87320-145">Uppfærið færsluna í forriti viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87320-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="87320-146">Nýja athugasemdin ætti að sjást í tímalínunni.</span><span class="sxs-lookup"><span data-stu-id="87320-146">You should find the new note on the timeline.</span></span>

    ![Ný athugasemd á tímalínunni í forriti viðskiptavinar](media/notes-fo-3.png)

<span data-ttu-id="87320-148">Hægt er að flokka athugasemd sem annaðhvort innri eða ytri.</span><span class="sxs-lookup"><span data-stu-id="87320-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="87320-149">Í Finance and Operations-forritinu, á síðunni **Viðhengi**, skal opna athugasemdina og síðan í reitnum **Takmörkun** skal velja **Innri** eða **Ytri**.</span><span class="sxs-lookup"><span data-stu-id="87320-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Takmörkunarreitur](media/notes-fo-4.png)

<span data-ttu-id="87320-151">Einnig er hægt að búa til vefslóð.</span><span class="sxs-lookup"><span data-stu-id="87320-151">You can also create a URL.</span></span>

1. <span data-ttu-id="87320-152">Í Finance and Operations-forritinu, á síðunni **Viðhengi**, skal velja **Ný** \> **Vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="87320-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="87320-153">Færið inn titil og vefslóð.</span><span class="sxs-lookup"><span data-stu-id="87320-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="87320-154">Í reitnum **Takmörkun** skal velja **Innri** eða **Ytri**.</span><span class="sxs-lookup"><span data-stu-id="87320-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Vefslóð búin til í Finance and Operations-forritinu](media/notes-fo-5.png)

4. <span data-ttu-id="87320-156">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="87320-156">Select **Save**.</span></span>

    <span data-ttu-id="87320-157">Þar sem forrit viðskiptavina eru ekki með vefslóðargerð, er vefslóðin samþætt með tvöfaldri skráningu sem athugasemd.</span><span class="sxs-lookup"><span data-stu-id="87320-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![Vefslóð sem birtist sem athugasemd í forriti viðskiptavinar](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="87320-159">Skráarviðhengi eru ekki studd.</span><span class="sxs-lookup"><span data-stu-id="87320-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="87320-160">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="87320-160">Templates</span></span>

<span data-ttu-id="87320-161">Samþætting athugasemdar inniheldur safn af töfluvörpunum sem vinnur saman í gagnasamskiptum eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="87320-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="87320-162">Finance and Operations-forritið</span><span class="sxs-lookup"><span data-stu-id="87320-162">Finance and Operations app</span></span> | <span data-ttu-id="87320-163">Forrit viðskiptavinatengsla</span><span class="sxs-lookup"><span data-stu-id="87320-163">Customer engagement app</span></span> | <span data-ttu-id="87320-164">lýsing</span><span class="sxs-lookup"><span data-stu-id="87320-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="87320-165">Fylgiskjöl viðskiptamanns</span><span class="sxs-lookup"><span data-stu-id="87320-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="87320-166">Skýringar</span><span class="sxs-lookup"><span data-stu-id="87320-166">Annotations</span></span> | <span data-ttu-id="87320-167">Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um viðskiptavini (bæði fyrir fyrirtæki og einstaklinga).</span><span class="sxs-lookup"><span data-stu-id="87320-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="87320-168">Viðhengd skjöl lánardrottins</span><span class="sxs-lookup"><span data-stu-id="87320-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="87320-169">Skýringar</span><span class="sxs-lookup"><span data-stu-id="87320-169">Annotations</span></span> | <span data-ttu-id="87320-170">Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um lánardrottna (bæði fyrir fyrirtæki og einstaklinga).</span><span class="sxs-lookup"><span data-stu-id="87320-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="87320-171">Viðhengt skjal fyrir sölupöntunarhaus</span><span class="sxs-lookup"><span data-stu-id="87320-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="87320-172">Skýringar</span><span class="sxs-lookup"><span data-stu-id="87320-172">Annotations</span></span> | <span data-ttu-id="87320-173">Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="87320-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="87320-174">Viðhengd skjöl fyrir haus innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="87320-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="87320-175">Skýringar</span><span class="sxs-lookup"><span data-stu-id="87320-175">Annotations</span></span> | <span data-ttu-id="87320-176">Fyrirtæki sem nota venjulegan texta og vefslóðir til að sækja upplýsingar um innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="87320-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="87320-177">Frekari upplýsingar er að finna í [Tilvísun vörpunar á tvöfaldri skráningu](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="87320-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
