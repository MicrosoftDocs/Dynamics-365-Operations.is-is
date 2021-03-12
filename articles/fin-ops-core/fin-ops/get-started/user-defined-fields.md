---
title: Stofna og vinna með sérstillt svæði
description: Þetta efnisatriði sýnir hvernig á að stofna sérsniðna reiti með notandaviðmóti til að laga forritið að sínum viðskiptum.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: eee5b072f999aab7d4a5e72888abad3915e03d5b
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798119"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="987ee-103">Stofna og vinna með sérstillt svæði</span><span class="sxs-lookup"><span data-stu-id="987ee-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="987ee-104">Þótt það sé víðtækt úrval reita út fyrir kassann til að stjórna fjölmörgum viðskiptaferlum, er stundum þörf fyrir fyrirtæki til að fylgjast með viðbótarupplýsingum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="987ee-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="987ee-105">Þó að hægt sé að nota forritara til að bæta við þessum reitum sem viðbætum í verkfærum framkvæmdaraðila, þá gerir eiginleiki sérsniðinna reita kleift að bæta við reitum beint úr notendaviðmóti og leyfa þér þannig að sérsníða forritið að viðskiptum þínum með vafranum þínum.</span><span class="sxs-lookup"><span data-stu-id="987ee-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="987ee-106">Möguleikinn til að bæta við sérstilltum svæðum er í boði í verkvangsuppfærslu 13 og síðar.</span><span class="sxs-lookup"><span data-stu-id="987ee-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="987ee-107">Aðeins notendur með sérstakar heimildir hafa aðgang að þessum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="987ee-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="987ee-108">Þetta myndband sýnir hversu auðvelt það er að bæta við sérsniðnum reit á síðu: [Bæta við sérsniðnum reitum í](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="987ee-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="987ee-109">Stofna sérstillt svæði</span><span class="sxs-lookup"><span data-stu-id="987ee-109">Creating custom fields</span></span>

<span data-ttu-id="987ee-110">Eftir að þú hefur auðkennt viðbótarupplýsingar sem þú vilt fylgjast með í forritinu getur þú búið til sérstillta svæðið á viðeigandi töflu og sýna nýja svæðið á síðu.</span><span class="sxs-lookup"><span data-stu-id="987ee-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="987ee-111">Eftirfarandi skref lýsa ferlinu við stofnun á sérstilltu svæði og koma þessu svæði fyrir á skjámynd.</span><span class="sxs-lookup"><span data-stu-id="987ee-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="987ee-112">Farðu á skjámyndina þar sem þörf er á nýja svæðinu.</span><span class="sxs-lookup"><span data-stu-id="987ee-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="987ee-113">Vegna þess að endamarkið er að sýna sérstillta svæðið á skjámynd, er inngangurinn að því að stofna sérstillt svæði í upplifun sérstillinga.</span><span class="sxs-lookup"><span data-stu-id="987ee-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="987ee-114">Opnaðu tækastiku sérstillinga með því að velja **Valkostir** og svo **Sérstilla þessa skjámynd**.</span><span class="sxs-lookup"><span data-stu-id="987ee-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="987ee-115">Smelltu á **Setja inn** og svo **Svæði**.</span><span class="sxs-lookup"><span data-stu-id="987ee-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="987ee-116">Veldu svæðið á skjámyndinni þar sem þú vilt sýna nýja svæðið.</span><span class="sxs-lookup"><span data-stu-id="987ee-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="987ee-117">Eftir valið birtir **Setja inn svæði** svarglugginn lista yfir núverandi svæði sem hægt er að setja inn á valda svæðið á skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="987ee-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="987ee-118">Gakktu úr skugga um að svæðið sem þú hefur áhuga á sé ekki nú þegar á listanum.</span><span class="sxs-lookup"><span data-stu-id="987ee-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="987ee-119">Ef svo er, geturðu einfaldlega valið þetta svæði í listanum og smellt á **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="987ee-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="987ee-120">Smelltu á **Búa til nýtt svæði** hnappinn fyrir ofan listann til að hefja ferlið við stofnun á sérstilltu svæði.</span><span class="sxs-lookup"><span data-stu-id="987ee-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="987ee-121">Þetta mun opna **Búa til nýtt svæði** svargluggann.</span><span class="sxs-lookup"><span data-stu-id="987ee-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="987ee-122">Ef þú sérð ekki **Búa til nýtt svæði** hnappinn hefur þú ekki nauðsynlegar heimildir til að nota þennan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="987ee-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="987ee-123">Sláðu inn eftirfarandi upplýsingar í svargluggann **Búa til nýtt svæði**.</span><span class="sxs-lookup"><span data-stu-id="987ee-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="987ee-124">Veldu gagnasafnstöflu þar sem bæta skal við þessari töflu.</span><span class="sxs-lookup"><span data-stu-id="987ee-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="987ee-125">Athugaðu að aðeins töflur sem styðja sérstillt svæði birtast í fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="987ee-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="987ee-126">Sjá kaflann hér að neðan til að fá tæknilegar upplýsingar um studdar töflur.</span><span class="sxs-lookup"><span data-stu-id="987ee-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="987ee-127">Veldu gagnagerðina fyrir nýja svæðið.</span><span class="sxs-lookup"><span data-stu-id="987ee-127">Select the data type for the new field.</span></span> <span data-ttu-id="987ee-128">Tiltækar gagnagerðir eru gátreitur, dagsetning, dagsetningartími, númer, tínslulisti og texti.</span><span class="sxs-lookup"><span data-stu-id="987ee-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="987ee-129">Ef þú velur gagngerðina texti getur þú einnig tilgreint hámarkslengd textans sem hægt er að slá inn í þetta svæði.</span><span class="sxs-lookup"><span data-stu-id="987ee-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="987ee-130">Ef þú velur gagnagerðina tínslulisti getur þú einnig valið sett af gildum sem gilda fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="987ee-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="987ee-131">Gefðu svæðinu heiti, merkimiða og hjálpartexta.</span><span class="sxs-lookup"><span data-stu-id="987ee-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="987ee-132">Heitið samsvarar áþreifanlegu heiti svæðis í gagnagrunninum, en merkimiðinn og hjálpartextinn eru textinn sem er notaður til að tákna þetta svæði í notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="987ee-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="987ee-133">Ef þetta er eina svæðið sem þú þarft að stofna fyrir þessa skjámynd, skaltu smella á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="987ee-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="987ee-134">Ef þú þarft að stofna fleiri svæði skaltu smella á **Vista og nýtt** og fara aftur í skref 7.</span><span class="sxs-lookup"><span data-stu-id="987ee-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="987ee-135">Athugaðu að það er nú takmarkað við **20 sérstillt svæði á hverja töflu**.</span><span class="sxs-lookup"><span data-stu-id="987ee-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="987ee-136">Að fara úr **Búa til nýtt svæði** svarglugganum skilar þér aftur í **Setja inn svæði** svargluggann.</span><span class="sxs-lookup"><span data-stu-id="987ee-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="987ee-137">Sérhvert sérstillt svæði sem var bætt við verður sjálfkrafa merkt í svæðislistanum sem á að setja inn á skjámyndina.</span><span class="sxs-lookup"><span data-stu-id="987ee-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="987ee-138">Smelltu á **Setja inn** til að setja inn merktu reitina í valda svæðið á forminu.</span><span class="sxs-lookup"><span data-stu-id="987ee-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="987ee-139">**Valfrjálst:** Virkjaðu **Færa** stillinguna frá tækjastiku sérstillinga til að færa nýju reitina á viðkomandi stað á valda svæðinu.</span><span class="sxs-lookup"><span data-stu-id="987ee-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="987ee-140">Sjá [Sérsníða notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um hvernig á að nota hinar ýmsu sérstillingar til að hagræða formi til persónulegrar notkunar.</span><span class="sxs-lookup"><span data-stu-id="987ee-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="987ee-141">Deiling sérsniðinna reita með öðrum notendum</span><span class="sxs-lookup"><span data-stu-id="987ee-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="987ee-142">Eftir að þú hefur búið til sérsniðinn reit og birt hann á sniði gætirðu viljað veita þennan uppfæra síðuskjá sem inniheldur nýja reitinn fyrir aðra notendur í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="987ee-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="987ee-143">Þetta er hægt að framkvæma á tvenns konar hátt með því að nota sérstillingarvalkosti vörunnar:</span><span class="sxs-lookup"><span data-stu-id="987ee-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="987ee-144">Ráðlögð leið er í gegnum kerfisstjóra, sem getur ýtt sérsniðum til allra notenda eða undirhóps notenda.</span><span class="sxs-lookup"><span data-stu-id="987ee-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="987ee-145">Sjá [Sérsníða notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="987ee-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="987ee-146">Einnig er hægt að flytja út breytingarnar þínar (kallast *sérstillingar*), senda þær á einn eða fleiri notendur og láta hvern notanda flytja inn breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="987ee-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="987ee-147">**Stjórna** valkosturinn á tækjastiku sérstillinga gerir þér kleift að flytja út og flytja inn sérstillingar.</span><span class="sxs-lookup"><span data-stu-id="987ee-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="987ee-148">Stjórna sérstilltum svæðum</span><span class="sxs-lookup"><span data-stu-id="987ee-148">Managing custom fields</span></span>

<span data-ttu-id="987ee-149">Stjórnun allra sérstilltra svæði í kerfinu er hægt að gera með **Sérstillt svæði** síðunni í kerfisstjórnunareiningunni.</span><span class="sxs-lookup"><span data-stu-id="987ee-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="987ee-150">Þessi síða leyfir notendum aðgang að mörgum möguleikum, þar á meðal:</span><span class="sxs-lookup"><span data-stu-id="987ee-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="987ee-151">Skoða lista yfir öll sérstillt svæði í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="987ee-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="987ee-152">Takmarkaðar breytingar á núverandi sérstilltum svæðum.</span><span class="sxs-lookup"><span data-stu-id="987ee-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="987ee-153">Eyða sérstilltum svæðum.</span><span class="sxs-lookup"><span data-stu-id="987ee-153">Deleting custom fields.</span></span>
- <span data-ttu-id="987ee-154">Birta sérstillt svæði á gagnaeiningum.</span><span class="sxs-lookup"><span data-stu-id="987ee-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="987ee-155">Veita þýðingar á merkimiðum sérstilltra svæða og hjálpartexta.</span><span class="sxs-lookup"><span data-stu-id="987ee-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="987ee-156">Skoða öll sérstillt svæði</span><span class="sxs-lookup"><span data-stu-id="987ee-156">Viewing all custom fields</span></span>

<span data-ttu-id="987ee-157">**Sérstillt svæði** síðan veitir sýnileika til allra sérstilltu svæðanna sem hafa verið skilgreind í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="987ee-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="987ee-158">Veldu einfaldlega töfluna sem þú hefur áhuga á og síðan mun uppfærast og birta lista yfir sérstilltu svæðin sem tengjast þessari töflu.</span><span class="sxs-lookup"><span data-stu-id="987ee-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="987ee-159">Velja sérstillt svæði úr listanum mun leyfa þér að skoða allar upplýsingar um svæðið.</span><span class="sxs-lookup"><span data-stu-id="987ee-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="987ee-160">Breyti sérstilltum svæðum</span><span class="sxs-lookup"><span data-stu-id="987ee-160">Editing custom fields</span></span>

<span data-ttu-id="987ee-161">Eftir að sérstillt svæði hefur verið stofnað mun aðeins vera hægt að breyta ákveðnum upplýsingum um sérstilltu svæðin á **Sérstillt svæði** síðunni.</span><span class="sxs-lookup"><span data-stu-id="987ee-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="987ee-162">Þú *getur* breytt þessum eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="987ee-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="987ee-163">Merkimiði</span><span class="sxs-lookup"><span data-stu-id="987ee-163">Label</span></span>
- <span data-ttu-id="987ee-164">Hjálpartexti</span><span class="sxs-lookup"><span data-stu-id="987ee-164">Help text</span></span>
- <span data-ttu-id="987ee-165">Lengd, fyrir textasvæði</span><span class="sxs-lookup"><span data-stu-id="987ee-165">Length, for Text fields</span></span>

<span data-ttu-id="987ee-166">Þú *getur ekki* breytt eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="987ee-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="987ee-167">Heiti reits</span><span class="sxs-lookup"><span data-stu-id="987ee-167">Field name</span></span>
- <span data-ttu-id="987ee-168">Gagnagerð</span><span class="sxs-lookup"><span data-stu-id="987ee-168">Data type</span></span>

<span data-ttu-id="987ee-169">Að auki, fyrir svæði tínslulista, er hægt að endurskipuleggja gildu gildin fyrir sérstillta svæðið og hægt er að bæta við nýjum gildum; ekki er hægt að fjarlægja núverandi gildi á tínslulistanum.</span><span class="sxs-lookup"><span data-stu-id="987ee-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="987ee-170">Mundu að smella á **Virkja breytingar** þegar þú ert búinn að breyta svæðum fyrir tiltekna töflu þannig að breytingarnar verði vistaðar.</span><span class="sxs-lookup"><span data-stu-id="987ee-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="987ee-171">Birtu sérstillt svæði í gagnaeiningum</span><span class="sxs-lookup"><span data-stu-id="987ee-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="987ee-172">Það kann einnig að vera mikilvægt að leyfa sérstilltum svæðum að vera sýnileg á gagnaeiningum.</span><span class="sxs-lookup"><span data-stu-id="987ee-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="987ee-173">Gagnaeiningar eru notaðar í [Yfirlit yfir Office-samþættingu](../../dev-itpro/office-integration/office-integration.md) eiginleikanum, sem og fyrir inn- og útflutning á gögnum framvinduna.</span><span class="sxs-lookup"><span data-stu-id="987ee-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="987ee-174">Fylgdu þessum skrefum til að sýna sérstillt svæði á gagnaeiningu:</span><span class="sxs-lookup"><span data-stu-id="987ee-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="987ee-175">Veldu sérstilltu svæðin **Sérstillt svæði** skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="987ee-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="987ee-176">Stækkaðu **Einingar** kaflann til að skoða hóp eininga sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="987ee-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="987ee-177">Smelltu á hnappinn **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="987ee-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="987ee-178">Breyttu **Virkjað** svæðinu svo það sé valið fyrir hverja einingu sem ætti að sýna þetta svæði.</span><span class="sxs-lookup"><span data-stu-id="987ee-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="987ee-179">Smelltu á **Virkja breytingar** til að vista val þitt.</span><span class="sxs-lookup"><span data-stu-id="987ee-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="987ee-180">Leyfir sérstilltum svæðum að birtast á öðrum tungumálum</span><span class="sxs-lookup"><span data-stu-id="987ee-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="987ee-181">Vegna þess að sérstillt svæði gætu þurft að vera opnuð af notendum á mismunandi tungumálum, **Sérstillt svæði** reiturinn býður upp á þýðingar á merkimiðum og hjálpartextum yfir á önnur tungumál.</span><span class="sxs-lookup"><span data-stu-id="987ee-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="987ee-182">Eftirfarandi skref lýsa þýðingaferlinu á sérstilltum svæðum á öðrum tungumálum:</span><span class="sxs-lookup"><span data-stu-id="987ee-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="987ee-183">Veldu sérstilltu svæðin á **Serstillt svæði** síðunni.</span><span class="sxs-lookup"><span data-stu-id="987ee-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="987ee-184">Veldu **Þýðingar** hnappinn í aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="987ee-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="987ee-185">Þetta mun opna fellilista valmyndar með núverandi þýðingar fyrir þetta svæði.</span><span class="sxs-lookup"><span data-stu-id="987ee-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="987ee-186">**TUNGUMÁLA** fellilisti valmyndar sýnir tungumálin sem hefur verið þýtt á að svo stöddu.</span><span class="sxs-lookup"><span data-stu-id="987ee-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="987ee-187">Ef þú vilt breyta núverandi þýðingu skaltu velja viðeigandi tungumál úr valmyndinni og breyta inntakinu fyrir merkimiðann og hjálpartextann.</span><span class="sxs-lookup"><span data-stu-id="987ee-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="987ee-188">Annars skaltu smella á **Bæta við tungumáli** hnappinn, veldu viðkomandi tungumál úr valmyndinni og þýddu svo inntakið fyrir merkimiðann og hjálpartextann.</span><span class="sxs-lookup"><span data-stu-id="987ee-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="987ee-189">Smelltu á **OK** þegar þú ert búin/n.</span><span class="sxs-lookup"><span data-stu-id="987ee-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="987ee-190">Eyða sérstilltum svæðum</span><span class="sxs-lookup"><span data-stu-id="987ee-190">Deleting custom fields</span></span>

<span data-ttu-id="987ee-191">Í sumum sjaldgæfum tilfellum gætir þú ákveðið að ekki sé lengur þörf á sérstilltum svæðum.</span><span class="sxs-lookup"><span data-stu-id="987ee-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="987ee-192">Þegar það á við getur kerfisstjóri valið að eyða svæðinu af **Sérstillt svæði** síðunni.</span><span class="sxs-lookup"><span data-stu-id="987ee-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="987ee-193">Til að gera þetta skaltu tryggja að rétt svæði sé valið, smelltu á **Eyða**, smelltu á **Já** til að staðfesta eyðingu og smelltu loks á **Virkja breytingar**.</span><span class="sxs-lookup"><span data-stu-id="987ee-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="987ee-194">Ekki er hægt að afturkalla þessa aðgerð og hún mun leiða til þess að gögnin sem tengjast svæðinu verði varanlega eytt úr gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="987ee-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="987ee-195">Viðauki</span><span class="sxs-lookup"><span data-stu-id="987ee-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="987ee-196">Hver getur búið til sérstillt svæði?</span><span class="sxs-lookup"><span data-stu-id="987ee-196">Who can create custom fields?</span></span>

<span data-ttu-id="987ee-197">Til að vernda kerfið, getur aðeins kerfisstjóri stofnað sérstillt svæði.</span><span class="sxs-lookup"><span data-stu-id="987ee-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="987ee-198">Hins vegar geta þessi kraftnotendur, sem fyrirtækið telur nauðsynlega, fengið réttindi til að stofna sérstillt svæði í gegnum kerfisstjóra með því að nota öryggishlutverkið **Sérstillingar keyrslutíma fyrir kraftnotendur**.</span><span class="sxs-lookup"><span data-stu-id="987ee-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="987ee-199">Notendur án þessa öryggishlutverks geta ekki stofnað sérstillt svæði, en munu samt geta séð og átt við sérstillt svæði sem aðrir notendur í kerfinu hafa bætt við.</span><span class="sxs-lookup"><span data-stu-id="987ee-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="987ee-200">Hvað töflur styðja sérstillt svæði?</span><span class="sxs-lookup"><span data-stu-id="987ee-200">What tables support custom fields?</span></span>

<span data-ttu-id="987ee-201">Út af frammistöðu og tæknilegum ástæðum leyfa aðeins töflur sem uppfylla eftirfarandi núgildandi skilyrði sérstilltum svæðum að vera bætt við.</span><span class="sxs-lookup"><span data-stu-id="987ee-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="987ee-202">Taflan verður að vera merkt sem einn af þessum hópum:</span><span class="sxs-lookup"><span data-stu-id="987ee-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="987ee-203">Hópur</span><span class="sxs-lookup"><span data-stu-id="987ee-203">Group</span></span>
    - <span data-ttu-id="987ee-204">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="987ee-204">WorksheetHeader</span></span>
    - <span data-ttu-id="987ee-205">Aðal</span><span class="sxs-lookup"><span data-stu-id="987ee-205">Main</span></span>
    - <span data-ttu-id="987ee-206">Ýmislegt</span><span class="sxs-lookup"><span data-stu-id="987ee-206">Miscellaneous</span></span>
    - <span data-ttu-id="987ee-207">Færibreyta</span><span class="sxs-lookup"><span data-stu-id="987ee-207">Parameter</span></span>
    - <span data-ttu-id="987ee-208">Tilvísun</span><span class="sxs-lookup"><span data-stu-id="987ee-208">Reference</span></span>
    - <span data-ttu-id="987ee-209">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="987ee-209">TransactionHeader</span></span>

- <span data-ttu-id="987ee-210">Taflan getur ekki víkkað út aðra töflu.</span><span class="sxs-lookup"><span data-stu-id="987ee-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="987ee-211">Ekki er hægt að merkja töfluna sem kerfistöflu.</span><span class="sxs-lookup"><span data-stu-id="987ee-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="987ee-212">Taflan getur ekki verið tímabundin tafla.</span><span class="sxs-lookup"><span data-stu-id="987ee-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="987ee-213">Get ég vísað til sérsniðinna reita úr forritunartólunum?</span><span class="sxs-lookup"><span data-stu-id="987ee-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="987ee-214">Aðeins er hægt að stjórna sérsniðnum reitum í gegnum notendaviðmótið og ekki er hægt að vísa í þá með kóða.</span><span class="sxs-lookup"><span data-stu-id="987ee-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 
