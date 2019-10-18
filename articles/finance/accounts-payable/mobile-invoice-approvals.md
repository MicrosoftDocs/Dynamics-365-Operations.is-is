---
title: Reikningssamþykktir í fartækjum
description: Í þessu efnisatriði er ætlað að gefa praktíska nálgun til að hanna farsímaaðstæður með því að taka reikningssamþykktir fyrir fartæki sem notkunartilvik.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 956c866a6b39e2a81f085910e00d2bfe8683829c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178357"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="11e31-103">Reikningssamþykktir í fartækjum</span><span class="sxs-lookup"><span data-stu-id="11e31-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11e31-104">Farsímageta gerir fyrirtækjanotenda kleift að hanna farsímaupplifun.</span><span class="sxs-lookup"><span data-stu-id="11e31-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="11e31-105">Fyrir ítarlegri dæmi leyfir kerfið forriturum einnig að framlengja getu eins og þeir vilja.</span><span class="sxs-lookup"><span data-stu-id="11e31-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="11e31-106">Skilvirkasta leiðin til að læra sum af nýju hugtökunum í fartæki er að fara gegnum ferlið að hanna ný dæmi.</span><span class="sxs-lookup"><span data-stu-id="11e31-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="11e31-107">Í þessu efnisatriði er ætlað að gefa praktíska nálgun til að hanna farsímaaðstæður með því að taka reikningssamþykktir fyrir fartæki sem notkunartilvik.</span><span class="sxs-lookup"><span data-stu-id="11e31-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="11e31-108">Þetta efnisatriði á að aðstoða við hönnun á öðrum frávikum á aðstæðum og einnig er hægt að nota það í öðrum aðstæðum sem eru ekki eru tengdar reikningum lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="11e31-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="11e31-109">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="11e31-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="11e31-110">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="11e31-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="11e31-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="11e31-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e31-112">Fyrirframlestur farsímahandbókar</span><span class="sxs-lookup"><span data-stu-id="11e31-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="11e31-113">Fartækjaverkvangur</span><span class="sxs-lookup"><span data-stu-id="11e31-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="11e31-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="11e31-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="11e31-115">Vertu viss um að þú sért að nota umhverfi sem er með útgáfu 1611 og uppfærslu verkvangs 3 (nóvember 2016).</span><span class="sxs-lookup"><span data-stu-id="11e31-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="11e31-116">Setja upp bráðabót KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="11e31-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="11e31-117">Verkskráning getur skráð rangt tvær Loka skipanir fyrir felliglugga; þetta er innifalið í uppfærslu verkvangs 3 (uppfærsla nóvember 2016).</span><span class="sxs-lookup"><span data-stu-id="11e31-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="11e31-118">Setja upp bráðabót KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="11e31-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="11e31-119">Þessi bráðabót leyfir að viðhengi séu skoðuð í farsímabiðlara; þetta er innifalið í uppfærslu verkvangs 3 (uppfærsla í nóvember 2016).</span><span class="sxs-lookup"><span data-stu-id="11e31-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="11e31-120">Setja upp bráðabót KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="11e31-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="11e31-121">Forritakóði fyrir farsímasamþykkt reiknings lánardrottins; þetta er innifalið í útgáfu 7.0.1 (maí 2016).</span><span class="sxs-lookup"><span data-stu-id="11e31-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="11e31-122">Í tæki með Android eða iOS eða Windows sem er með farsímaforritið sem er uppsett.</span><span class="sxs-lookup"><span data-stu-id="11e31-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="11e31-123">Leita að forritinu í viðeigandi forritaverslun.</span><span class="sxs-lookup"><span data-stu-id="11e31-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="11e31-124">Inngangur</span><span class="sxs-lookup"><span data-stu-id="11e31-124">Introduction</span></span>
<span data-ttu-id="11e31-125">Farsímasamþykktir fyrir reikninga lánardrottins þurfa þrjár bráðabætur sem nefndar eru í hlutanum „Forkröfur“.</span><span class="sxs-lookup"><span data-stu-id="11e31-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="11e31-126">Þessar bráðabætur veita ekki vinnusvæði fyrir reikningssamþykki.</span><span class="sxs-lookup"><span data-stu-id="11e31-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="11e31-127">Til að læra hvað vinnusvæði er í samhengi við fartæki, skaltu lesa farsímahandbókina sem er nefnd í hlutanum „Forkröfur“.</span><span class="sxs-lookup"><span data-stu-id="11e31-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="11e31-128">Vinnusvæði reikningssamþykkta verður að vera hannað.</span><span class="sxs-lookup"><span data-stu-id="11e31-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="11e31-129">Hvert fyrirtæki skipuleggur og skilgreinir mismunandi viðskiptaferli fyrir reikninga lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="11e31-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="11e31-130">Áður en farsímaupplifun fyrir samþykktir reiknings lánardrottins er hönnuð ætti að íhuga að eftirfarandi þætti viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="11e31-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="11e31-131">Hugmyndin er að nota þessa gagnapunkta eins mikið og hægt er til að hámarka reynslu notanda á tækinu.</span><span class="sxs-lookup"><span data-stu-id="11e31-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="11e31-132">Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="11e31-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="11e31-133">Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="11e31-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="11e31-134">Hversu margar reikningslínur eru í reikningi?</span><span class="sxs-lookup"><span data-stu-id="11e31-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="11e31-135">Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.</span><span class="sxs-lookup"><span data-stu-id="11e31-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="11e31-136">Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum?</span><span class="sxs-lookup"><span data-stu-id="11e31-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="11e31-137">Ef svarið þessari spurningu er já, íhugið eftirfarandi spurningar:</span><span class="sxs-lookup"><span data-stu-id="11e31-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="11e31-138">Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld, skipti og svo framvegis) eru fyrir reikningslínu?</span><span class="sxs-lookup"><span data-stu-id="11e31-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="11e31-139">Aftur skal nota 80-20 reglu.</span><span class="sxs-lookup"><span data-stu-id="11e31-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="11e31-140">Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings?</span><span class="sxs-lookup"><span data-stu-id="11e31-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="11e31-141">Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?</span><span class="sxs-lookup"><span data-stu-id="11e31-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="11e31-142">Þetta efnisatriði útskýrir ekki hvernig á að breyta dreifingu fjárhagsupphæða þar sem þessi virkni er ekki studd eins og stendur fyrir farsímaaðstæður.</span><span class="sxs-lookup"><span data-stu-id="11e31-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="11e31-143">Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?</span><span class="sxs-lookup"><span data-stu-id="11e31-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="11e31-144">Hönnun farsímareynslu fyrir reikningssamþykktir verður mismunandi, eftir því hver svörin verða við þessum spurningum.</span><span class="sxs-lookup"><span data-stu-id="11e31-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="11e31-145">Markmiðið er að fínstilla reynslu notanda fyrir viðskiptaferli í fartæki innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="11e31-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="11e31-146">Í afganginum af þessu efnisatriði skoðum við tvær frávikaaðstæður sem byggjast á mismunandi svörum við spurningunum hér á undan.</span><span class="sxs-lookup"><span data-stu-id="11e31-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="11e31-147">Almennt séð, þegar unnið er með farsímahönnuði, þarf að ganga úr skugga um að 'birta' breytingarnar til að koma í veg fyrir uppfærslur mistakist.</span><span class="sxs-lookup"><span data-stu-id="11e31-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="11e31-148">Hönnun á einföldum aðstæðum reikningssamþykktar fyrir Contoso</span><span class="sxs-lookup"><span data-stu-id="11e31-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11e31-149">Sviðsmyndareigind</span><span class="sxs-lookup"><span data-stu-id="11e31-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="11e31-150">Svara</span><span class="sxs-lookup"><span data-stu-id="11e31-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11e31-151">Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="11e31-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="11e31-152">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11e31-152">Vendor name</span></span></li>
<li><span data-ttu-id="11e31-153">Heildarupphæð reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-153">Invoice total</span></span></li>
<li><span data-ttu-id="11e31-154">Reikningslykill</span><span class="sxs-lookup"><span data-stu-id="11e31-154">Invoice account</span></span></li>
<li><span data-ttu-id="11e31-155">Númer reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-155">Invoice number</span></span></li>
<li><span data-ttu-id="11e31-156">Reikningsdagsetning</span><span class="sxs-lookup"><span data-stu-id="11e31-156">Invoice date</span></span></li>
<li><span data-ttu-id="11e31-157">Lýsing reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-157">Invoice description</span></span></li>
<li><span data-ttu-id="11e31-158">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="11e31-158">Due date</span></span></li>
<li><span data-ttu-id="11e31-159">Gjaldmiðill reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e31-160">Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="11e31-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="11e31-161">Innkaupategund</span><span class="sxs-lookup"><span data-stu-id="11e31-161">Procurement category</span></span></li>
<li><span data-ttu-id="11e31-162">Magn</span><span class="sxs-lookup"><span data-stu-id="11e31-162">Quantity</span></span></li>
<li><span data-ttu-id="11e31-163">Einingarverð</span><span class="sxs-lookup"><span data-stu-id="11e31-163">Unit price</span></span></li>
<li><span data-ttu-id="11e31-164">Nettóupphæð línu</span><span class="sxs-lookup"><span data-stu-id="11e31-164">Line net amount</span></span></li>
<li><span data-ttu-id="11e31-165">Upphæð 1099</span><span class="sxs-lookup"><span data-stu-id="11e31-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11e31-166">Hversu margar reikningslínur eru í reikningi?</span><span class="sxs-lookup"><span data-stu-id="11e31-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="11e31-167">Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.</span><span class="sxs-lookup"><span data-stu-id="11e31-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="11e31-168">1</span><span class="sxs-lookup"><span data-stu-id="11e31-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e31-169">Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum?</span><span class="sxs-lookup"><span data-stu-id="11e31-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="11e31-170">Já</span><span class="sxs-lookup"><span data-stu-id="11e31-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11e31-171">Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld og svo framvegis) eru fyrir reikningslínuna?</span><span class="sxs-lookup"><span data-stu-id="11e31-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="11e31-172">Aftur skal nota 80-20 reglu.</span><span class="sxs-lookup"><span data-stu-id="11e31-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="11e31-173">Heildarverð: 2 vsk: 0 Gjöld: 0</span><span class="sxs-lookup"><span data-stu-id="11e31-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e31-174">Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings?</span><span class="sxs-lookup"><span data-stu-id="11e31-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="11e31-175">Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?</span><span class="sxs-lookup"><span data-stu-id="11e31-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="11e31-176">Ekki notað</span><span class="sxs-lookup"><span data-stu-id="11e31-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11e31-177">Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?</span><span class="sxs-lookup"><span data-stu-id="11e31-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="11e31-178">Já</span><span class="sxs-lookup"><span data-stu-id="11e31-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="11e31-179">Stofna vinnusvæðið</span><span class="sxs-lookup"><span data-stu-id="11e31-179">Create the workspace</span></span>

1.  <span data-ttu-id="11e31-180">Í vafra og skráðu þig inn í forritið.</span><span class="sxs-lookup"><span data-stu-id="11e31-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="11e31-181">Eftir að notandi hefur verið skráður bæta **&mode = fartæki** vefslóð eins og sýnt er í eftirfarandi dæmi og endurnýja þarf síðuna: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="11e31-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="11e31-182">Smellið á hnappinn **Stillingar** (tannhjól) í efst til hægri á síðunni og smelltu svo á **Fartæki forrits**.</span><span class="sxs-lookup"><span data-stu-id="11e31-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="11e31-183">Hönnuður fartæki forrits verður birtast eins og Verkskráning birtist.</span><span class="sxs-lookup"><span data-stu-id="11e31-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="11e31-184">Smelltu á **Bæta við** til að búa til nýtt vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="11e31-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="11e31-185">Í þessu dæmi er vinnusvæðinu gefið heitið **Samþykktir**.</span><span class="sxs-lookup"><span data-stu-id="11e31-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="11e31-186">Færðu inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="11e31-186">Enter a description.</span></span>
6.  <span data-ttu-id="11e31-187">Velja lit vinnusvæðis</span><span class="sxs-lookup"><span data-stu-id="11e31-187">Select a workspace color.</span></span> <span data-ttu-id="11e31-188">Litur vinnusvæðisins verður notaður fyrir heildarstíl fyrir farsímareynslu fyrir þetta vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="11e31-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="11e31-189">Velja tákn fyrir vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="11e31-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="11e31-190">Smelltu á **Lokið**</span><span class="sxs-lookup"><span data-stu-id="11e31-190">Click **Done**</span></span>
9.  <span data-ttu-id="11e31-191">Smelltu á **Birta vinnusvæði** til að vista breytingarnar</span><span class="sxs-lookup"><span data-stu-id="11e31-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="11e31-192">Reikningar lánardrottins tengdir notanda</span><span class="sxs-lookup"><span data-stu-id="11e31-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="11e31-193">Fyrsta farsímasíðan sem ætti að hanna er listi yfir reikninga sem eru úthlutaðir notandanum til skoðunar.</span><span class="sxs-lookup"><span data-stu-id="11e31-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="11e31-194">Til að hanna þessa farsímasíðu notarðu síðuna **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="11e31-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="11e31-195">Áður en lokið er við þetta ferli skal ganga úr skugga um að a.m.k. einn lánardrottinsreikningur sé úthlutaður til þín til skoðunar og að reikningslínan hafi tvær dreifingar.</span><span class="sxs-lookup"><span data-stu-id="11e31-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="11e31-196">Þessi uppsetning uppfyllir kröfur fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="11e31-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="11e31-197">Í vefslóðinni skal skipta út heiti valmyndaratriðis með **VendMobileInvoiceAssignedToMeListPage** til að opna farsímaútgáfu af listasíðunni **Biðreikningar lánardrottins sem mér eru úthlutaðir** í kerfiseiningunni **Viðskiptaskuldir**.</span><span class="sxs-lookup"><span data-stu-id="11e31-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="11e31-198">Það fer eftir fjölda reikninga sem er úthlutað til þín í kerfinu en þessi síða sýnir þá reikninga.</span><span class="sxs-lookup"><span data-stu-id="11e31-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="11e31-199">Til að finna tilgreindan reikning er hægt að nota síuna til vinstri.</span><span class="sxs-lookup"><span data-stu-id="11e31-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="11e31-200">Hins vegar þurfum við ekki tilgreindan reikning fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="11e31-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="11e31-201">Við þurfum bara reikning sem úthlutað er til þín, sem gerir þér kleift að hanna farsímasíðuna.</span><span class="sxs-lookup"><span data-stu-id="11e31-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="11e31-202">Nýjar síður sem eru tiltækar hafa verið hannaðar sérstaklega fyrir þróun farsímaaðstæðna fyrir reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="11e31-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="11e31-203">Þess vegna verður að nota þessar síður.</span><span class="sxs-lookup"><span data-stu-id="11e31-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="11e31-204">Vefslóð á að líkjast eftirfarandi slóð og þegar hún hefur verið færð inn, verður síðan sem birtist á skýringarmyndinni að birtast: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Biðreikninga lánardrottins sem mér eru úthlutaðir síðuna](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="11e31-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="11e31-205">Smellið á hnappinn **Stillingar** (tannhjól) í efra hægra horni síðunnar og svo á **Farsímaforrit**.</span><span class="sxs-lookup"><span data-stu-id="11e31-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="11e31-206">Veljið vinnustöð og smellið á **Breyta**</span><span class="sxs-lookup"><span data-stu-id="11e31-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="11e31-207">Smellið á **Bæta við síðu** til að stofna fyrstu farsímasíðuna.</span><span class="sxs-lookup"><span data-stu-id="11e31-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="11e31-208">Færið inn heiti, eins og **Mínar lánardrottnareikningar**, og lýsingu, eins og **Reikninga lánardrottins sem mér eru úthlutaðir til skoðunar**.</span><span class="sxs-lookup"><span data-stu-id="11e31-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="11e31-209">Smelltu á **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="11e31-209">Click **Done**.</span></span>
7.  <span data-ttu-id="11e31-210">Í farsímahönnuði, á flipanum **Svæði** er smellt á **Velja svæði**.</span><span class="sxs-lookup"><span data-stu-id="11e31-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="11e31-211">Dálkar á listasíðunni verða að líkjast eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="11e31-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="11e31-212">[![Dálkar á síðunni Reikningar lánardrottins í bið sem notanda hefur verið úthlutað](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="11e31-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="11e31-213">Bæta þarf dálkum af listasíðunni, sem verða að birtast notendum á farsímasíðunni.</span><span class="sxs-lookup"><span data-stu-id="11e31-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="11e31-214">Röðin sem þú bætir við er sú röð sem svæðin eru birt notanda.</span><span class="sxs-lookup"><span data-stu-id="11e31-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="11e31-215">Eina leiðin til að breyta röðun svæða verður með því að velja aftur öll svæði.</span><span class="sxs-lookup"><span data-stu-id="11e31-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="11e31-216">Samkvæmt kröfum fyrir þetta dæmi er eftirfarandi átta svæða krafist.</span><span class="sxs-lookup"><span data-stu-id="11e31-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="11e31-217">Hins vegar gæti sumum notendum þótt átta svæði of mikið af upplýsingum til að hafa í farsíma.</span><span class="sxs-lookup"><span data-stu-id="11e31-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="11e31-218">Þess vegna munum við aðeins sýna mikilvægustu svæðin í farsímalistayfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="11e31-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="11e31-219">Eftirstandandi svæði birtast í upplýsingayfirliti sem við munum hanna seinna.</span><span class="sxs-lookup"><span data-stu-id="11e31-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="11e31-220">Eins og stendur bætum við eftirfarandi svæðum við.</span><span class="sxs-lookup"><span data-stu-id="11e31-220">For now, we will add the following fields.</span></span> <span data-ttu-id="11e31-221">Smellið á plúsmerkið (**+**) í þessum dálkum til að bæta við farsíðu.</span><span class="sxs-lookup"><span data-stu-id="11e31-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="11e31-222">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11e31-222">Vendor name</span></span>
    - <span data-ttu-id="11e31-223">Heildarupphæð reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-223">Invoice total</span></span>
    - <span data-ttu-id="11e31-224">Reikningslykill</span><span class="sxs-lookup"><span data-stu-id="11e31-224">Invoice account</span></span>
    - <span data-ttu-id="11e31-225">Númer reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-225">Invoice number</span></span>
    - <span data-ttu-id="11e31-226">Reikningsdagsetning</span><span class="sxs-lookup"><span data-stu-id="11e31-226">Invoice date</span></span>

    <span data-ttu-id="11e31-227">Eftir að svæðum er bætt við síðuna verður farsímasíðan að líkjast eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="11e31-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="11e31-228">[![Síðan eftir að svæðum hefur verið bætt við](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="11e31-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="11e31-229">Einnig verður að bæta eftirfarandi dálkum við núna, svo að við getum virkjað verkflæðisaðgerðir síðar.</span><span class="sxs-lookup"><span data-stu-id="11e31-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="11e31-230">Sýna lokin verk</span><span class="sxs-lookup"><span data-stu-id="11e31-230">Show complete task</span></span>
    - <span data-ttu-id="11e31-231">Sýna úthlutað verk</span><span class="sxs-lookup"><span data-stu-id="11e31-231">Show delegate task</span></span>
    - <span data-ttu-id="11e31-232">Sýna afturkallað verk</span><span class="sxs-lookup"><span data-stu-id="11e31-232">Show recall task</span></span>
    - <span data-ttu-id="11e31-233">Sýna hafnað verk</span><span class="sxs-lookup"><span data-stu-id="11e31-233">Show reject task</span></span>
    - <span data-ttu-id="11e31-234">Sýna verk með umbeðin lok</span><span class="sxs-lookup"><span data-stu-id="11e31-234">Show request completion task</span></span>
    - <span data-ttu-id="11e31-235">Sýna endursent verk</span><span class="sxs-lookup"><span data-stu-id="11e31-235">Show resubmit task</span></span>

10. <span data-ttu-id="11e31-236">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="11e31-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="11e31-237">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="11e31-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="11e31-238">Smelltu á **Birta vinnusvæði** til að vista verkið.</span><span class="sxs-lookup"><span data-stu-id="11e31-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="11e31-239">Virkja **Birta samtölu á biðstöðu lánardrottins reiknings reikninga lista** í færibreytuskjámynd viðskiptaskulda undir **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="11e31-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="11e31-240">Athugið að aðeins með því að virkja þessa færibreytu verða reikningssamtölur reiknaðar til að birtast á listasíðu lánardrottnareikninga í bið.</span><span class="sxs-lookup"><span data-stu-id="11e31-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="11e31-241">Þetta er ný geta sem er hluti af frumskilyrðum bráðabóta 3208224.</span><span class="sxs-lookup"><span data-stu-id="11e31-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="11e31-242">Reikningsupplýsingar lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11e31-242">Vendor invoice details</span></span>

<span data-ttu-id="11e31-243">Til að hanna reikningsupplýsingasíðu fyrir farsíma skal nota síðuna **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="11e31-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="11e31-244">Athugið að það fer eftir fjölda reikninga sem er úthlutað til þín í kerfinu en þessi síða sýnir elsta reikninginn (reikninginn sem var stofnaður fyrst).</span><span class="sxs-lookup"><span data-stu-id="11e31-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="11e31-245">Til að finna tilgreindan reikning er hægt að nota síuna til vinstri.</span><span class="sxs-lookup"><span data-stu-id="11e31-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="11e31-246">Hins vegar þurfum við ekki tilgreindan reikning fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="11e31-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="11e31-247">Við þurfum bara reikningsgögn svo að við getum hannað farsímasíðuna.</span><span class="sxs-lookup"><span data-stu-id="11e31-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="11e31-248">[![Verkflæðissíða](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="11e31-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="11e31-249">Í vefslóðinni skal skipta út heiti valmyndaratriðis með **VendMobileInvoiceHeaderDetails** til að opna skjámyndina</span><span class="sxs-lookup"><span data-stu-id="11e31-249">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2. <span data-ttu-id="11e31-250">Opnið hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól).</span><span class="sxs-lookup"><span data-stu-id="11e31-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3. <span data-ttu-id="11e31-251">Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="11e31-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4. <span data-ttu-id="11e31-252">Veldu síðuna **Reikningar lánardrottna minna** sem þú bjóst til áður og smelltu síðan á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="11e31-252">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>
5. <span data-ttu-id="11e31-253">Á flipanum **Svæði** smellirðu á dálkhausinn **Hnitanet**.</span><span class="sxs-lookup"><span data-stu-id="11e31-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6. <span data-ttu-id="11e31-254">Smellið á **Eiginleikar &gt; Bæta við síðu**.</span><span class="sxs-lookup"><span data-stu-id="11e31-254">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="11e31-255">**Athugasemd:** Þegar smellt er á fyrirsögnina **Hnitanet** og síðu bætt við, er venslum við upplýsingasíðu sjálfvirkt komið á.</span><span class="sxs-lookup"><span data-stu-id="11e31-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7. <span data-ttu-id="11e31-256">Færðu inn síðutitill, eins og **Upplýsingar um reikning**, og lýsingu, eins og **Skoða línuupplýsingar og reikningshausinn**.</span><span class="sxs-lookup"><span data-stu-id="11e31-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8. <span data-ttu-id="11e31-257">Smellið á **Velja svæði**.</span><span class="sxs-lookup"><span data-stu-id="11e31-257">Click **Select fields**.</span></span> <span data-ttu-id="11e31-258">Athugið að röðin sem þú bætir við er sú röð sem svæðin verða birt notanda.</span><span class="sxs-lookup"><span data-stu-id="11e31-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="11e31-259">Eina leiðin til að breyta röðun svæða verður með því að velja aftur öll svæði.</span><span class="sxs-lookup"><span data-stu-id="11e31-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9. <span data-ttu-id="11e31-260">Bættu við eftirfarandi reitum úr haus, samkvæmt kröfum fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="11e31-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="11e31-261">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11e31-261">Vendor name</span></span>
   - <span data-ttu-id="11e31-262">Heildarupphæð reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-262">Invoice total</span></span>
   - <span data-ttu-id="11e31-263">Reikningslykill</span><span class="sxs-lookup"><span data-stu-id="11e31-263">Invoice account</span></span>
   - <span data-ttu-id="11e31-264">Númer reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-264">Invoice number</span></span>
   - <span data-ttu-id="11e31-265">Reikningsdagsetning</span><span class="sxs-lookup"><span data-stu-id="11e31-265">Invoice date</span></span>
   - <span data-ttu-id="11e31-266">Lýsing reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-266">Invoice description</span></span>
   - <span data-ttu-id="11e31-267">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="11e31-267">Due date</span></span>
   - <span data-ttu-id="11e31-268">Gjaldmiðill reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-268">Invoice currency</span></span>

10. <span data-ttu-id="11e31-269">Bæta við eftirfarandi svæðum úr línutöflunni á síðuna:</span><span class="sxs-lookup"><span data-stu-id="11e31-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="11e31-270">Innkaupategund</span><span class="sxs-lookup"><span data-stu-id="11e31-270">Procurement category</span></span>
    - <span data-ttu-id="11e31-271">Magn</span><span class="sxs-lookup"><span data-stu-id="11e31-271">Quantity</span></span>
    - <span data-ttu-id="11e31-272">Einingarverð</span><span class="sxs-lookup"><span data-stu-id="11e31-272">Unit price</span></span>
    - <span data-ttu-id="11e31-273">Nettóupphæð línu</span><span class="sxs-lookup"><span data-stu-id="11e31-273">Line net amount</span></span>
    - <span data-ttu-id="11e31-274">Upphæð 1099</span><span class="sxs-lookup"><span data-stu-id="11e31-274">1099 amount</span></span>

11. <span data-ttu-id="11e31-275">Eftir að öllum svæðum úr fyrri tvö skref hefur verið bætt við, smellið á **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="11e31-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="11e31-276">Dálkar á listasíðunni verða að líkjast eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="11e31-276">The page must resemble the following illustration.</span></span>
    <span data-ttu-id="11e31-277">[![Síðan eftir að svæðum hefur verið bætt við](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="11e31-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="11e31-278">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="11e31-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="11e31-279">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="11e31-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="11e31-280">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="11e31-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="11e31-281">Verkflæðisaðgerðir</span><span class="sxs-lookup"><span data-stu-id="11e31-281">Workflow actions</span></span>

<span data-ttu-id="11e31-282">Til að bæta við verkflæðisaðgerðum skal nota síðuna **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="11e31-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="11e31-283">Til að opna þessa síðu skal skipta út heiti valmyndaratriðis í vefslóð, eins og gert var áður.</span><span class="sxs-lookup"><span data-stu-id="11e31-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="11e31-284">Síðan skal opna hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól).</span><span class="sxs-lookup"><span data-stu-id="11e31-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="11e31-285">Fylgið þessum skrefum til að bæta við verkflæðisaðgerðum á upplýsingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="11e31-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="11e31-286">Þú verður að hafa reikninga úthlutaða þér með rétta stöðu svo að verkflæðisaðgerðir sem þú ætlar að hanna fyrir séu tiltækar þér.</span><span class="sxs-lookup"><span data-stu-id="11e31-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="11e31-287">Skráning verkflæðisaðgerða</span><span class="sxs-lookup"><span data-stu-id="11e31-287">Record workflow actions</span></span>
1.  <span data-ttu-id="11e31-288">Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="11e31-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="11e31-289">Veldu síðuna **Upplýsingar um reikning** sem þú stofnaðir áður og smelltu síðan á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="11e31-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="11e31-290">Á flipanum **Aðgerðir** er smellt á **Bæta aðgerð við**.</span><span class="sxs-lookup"><span data-stu-id="11e31-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="11e31-291">Færðu inn aðgerðatitill eins og **Samþykkja**, og lýsingu, eins og **Samþykkja reikninginn**.</span><span class="sxs-lookup"><span data-stu-id="11e31-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="11e31-292">Athugið að titill aðgerðarinnar sem er færður hér inn verður heiti aðgerðarinnar sem er birt notanda í farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="11e31-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="11e31-293">Smelltu á **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="11e31-293">Click **Done**.</span></span>
6.  <span data-ttu-id="11e31-294">Smellið á **Velja svæði**.</span><span class="sxs-lookup"><span data-stu-id="11e31-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="11e31-295">Fara í gegnum verkflæðisferlið í **VendMobileInvoiceHeaderDetails** síðunni og ljúka við aðgerðina sem óskað er að skrá.</span><span class="sxs-lookup"><span data-stu-id="11e31-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="11e31-296">Gangið úr skugga um að færa inn athugasemdir um verkflæðið meðan á því stendur þannig að athugasemdasvæðið sé einnig innifalið í farsímareynslunni.</span><span class="sxs-lookup"><span data-stu-id="11e31-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="11e31-297">Þegar aðgerð verkflæðis hefur verið keyrð er smellt á **Gert** að ljúka verkinu fyrir Valið svæði.</span><span class="sxs-lookup"><span data-stu-id="11e31-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="11e31-298">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="11e31-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="11e31-299">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="11e31-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="11e31-300">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="11e31-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="11e31-301">Endurtaktu fyrra skref til að skrá allar nauðsynlegar verkflæðisaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="11e31-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="11e31-302">Stofnaðu .js-skrá</span><span class="sxs-lookup"><span data-stu-id="11e31-302">Create a .js file</span></span>
1. <span data-ttu-id="11e31-303">Opna Notepad eða Microsoft Visual Studio og líma eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="11e31-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="11e31-304">Vista skýrsluna sem .js-skrá</span><span class="sxs-lookup"><span data-stu-id="11e31-304">Save the file as a .js file.</span></span> <span data-ttu-id="11e31-305">Þessi kóði gerir eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="11e31-305">This code does the following:</span></span>
    - <span data-ttu-id="11e31-306">Hann felur aukalega dálka sem tengjast verkflæði, sem við bættum við áður á fartæki listasíðu.</span><span class="sxs-lookup"><span data-stu-id="11e31-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="11e31-307">Við bættum þessum dálkum við svo að forritið hafi upplýsingar í samhengi og geti framkvæmt næsta skref.</span><span class="sxs-lookup"><span data-stu-id="11e31-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="11e31-308">Á grunni verkflæðisskrefsins sem er virkt notar það rök til að sýna aðeins þær aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="11e31-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="11e31-309">Heiti síðnanna og annarra stýringa í kóðanum verða að vera þau sömu og heitin í vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="11e31-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  <span data-ttu-id="11e31-310">Hlaða upp kóðaskrá á vinnusvæðið með því að velja flipann **Röklegt**</span><span class="sxs-lookup"><span data-stu-id="11e31-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="11e31-311">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="11e31-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="11e31-312">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="11e31-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="11e31-313">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="11e31-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="11e31-314">Viðhengi reiknings lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11e31-314">Vendor invoice attachments</span></span>

1. <span data-ttu-id="11e31-315">Smellið á hnappinn **Stillingar** (tannhjól) í efra hægra horni síðunnar og svo á **Farsímaforrit**.</span><span class="sxs-lookup"><span data-stu-id="11e31-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2. <span data-ttu-id="11e31-316">Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="11e31-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3. <span data-ttu-id="11e31-317">Veldu <strong>\*\*Síðuna Reikningsupplýsingar sem þú stofnaðir áður áðan og smelltu síðan \*\*Breyta</strong>.</span><span class="sxs-lookup"><span data-stu-id="11e31-317">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>
4. <span data-ttu-id="11e31-318">Stilltu valkostinn **Skjalastjórnun** á **Já** eins og sýnt er hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="11e31-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="11e31-319">**Athugasemd:** Ef ekki þarf að sýna viðhengi í fartækinu er hægt að hafa þennan valkost stilltan á **Nei**, sem er sjálfgefin stilling.</span><span class="sxs-lookup"><span data-stu-id="11e31-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   <span data-ttu-id="11e31-320">![Skjalastjórnun](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="11e31-320">![Document management](./media/docmanagement-216x300.png)</span></span>
5. <span data-ttu-id="11e31-321">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="11e31-321">Click **Done** to exit edit mode.</span></span>
6. <span data-ttu-id="11e31-322">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="11e31-322">Click **Back** and then **Done** to exit the workspace</span></span>
7. <span data-ttu-id="11e31-323">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="11e31-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="11e31-324">Línudreifingar fyrir reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11e31-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="11e31-325">Kröfur fyrir þetta dæmi staðfesta að það verða aðeins dreifingar á línustigi dreifingar og að reikningur verður alltaf með aðeins eina línu.</span><span class="sxs-lookup"><span data-stu-id="11e31-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="11e31-326">Þar sem þessar aðstæður eru einfaldar verður notendaupplifunin í fartækinu einnig að vera nógu einföld til að notandinn þurfi ekki að kafa niður nokkrum þrep til að skoða dreifingu.</span><span class="sxs-lookup"><span data-stu-id="11e31-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="11e31-327">Lánardrottnareikningar hafa þann valkost að sýna alla skiptingu úr haus reiknings.</span><span class="sxs-lookup"><span data-stu-id="11e31-327">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="11e31-328">Þessi reynsla er það sem þarf fyrir farsímaaðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="11e31-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="11e31-329">Þess vegna munum við nota síðuna **VendMobileInvoiceAllDistributionTree** til að hanna þennan hluta farsímaaðstæðnanna.</span><span class="sxs-lookup"><span data-stu-id="11e31-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="11e31-330">Þegar við þekkjum kröfurnar hjálpar það okkur að ákveða hvaða tiltekna síðu á að nota og hvernig á að fínstilla notandaupplifun farsíma nákvæmlega þegar við hönnum aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="11e31-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="11e31-331">Í seinni aðstæðunum munum við nota aðra síðu til að sýna dreifingarnar, þar sem kröfur fyrir þær aðstæður eru aðrar.</span><span class="sxs-lookup"><span data-stu-id="11e31-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="11e31-332">Í vefslóðinni skiptirðu út heiti valmyndaratriðis, eins og þú gerðir áður.</span><span class="sxs-lookup"><span data-stu-id="11e31-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="11e31-333">Síðan sem birtist á líkjast eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="11e31-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="11e31-334">[![Síðan Allar dreifingar](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="11e31-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="11e31-335">Opnið hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól).</span><span class="sxs-lookup"><span data-stu-id="11e31-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="11e31-336">Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="11e31-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="11e31-337">**Athugasemd:** Þú munt sjá að tvær nýjar síður voru sjálfkrafa stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="11e31-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="11e31-338">Kerfið stofnar þessar síður þar sem kveikt var á skjalastjórnun í fyrri hluta.</span><span class="sxs-lookup"><span data-stu-id="11e31-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="11e31-339">Þú mátt hunsa þessi nýjar síður.</span><span class="sxs-lookup"><span data-stu-id="11e31-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="11e31-340">Smella á **Bæta við síðu**.</span><span class="sxs-lookup"><span data-stu-id="11e31-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="11e31-341">Færa inn síðutitill, eins og **Skoða bókhald**, og lýsingu, eins og **Skoða bókhald fyrir reikning**.</span><span class="sxs-lookup"><span data-stu-id="11e31-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="11e31-342">Smelltu á **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="11e31-342">Click **Done**.</span></span>
7.  <span data-ttu-id="11e31-343">Á flipanum **Svæði** er smellt á **Velja svæði**, veljið eftirfarandi svæði af dreifingasíðunni og smellið síðan á **Gert**:</span><span class="sxs-lookup"><span data-stu-id="11e31-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="11e31-344">Upphæð</span><span class="sxs-lookup"><span data-stu-id="11e31-344">Amount</span></span>
    2.  <span data-ttu-id="11e31-345">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="11e31-345">Currency</span></span>
    3.  <span data-ttu-id="11e31-346">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="11e31-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="11e31-347">Við völdum ekki dálkinn **Lýsing** dálkur úr hnitaneti dreifinga, þar sem kröfur fyrir aðstæðurnar staðfestu að heildarverð er aðeins upphæðin sem dreifingar verða að vera fyrir.</span><span class="sxs-lookup"><span data-stu-id="11e31-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="11e31-348">Þess vegna krefst notandi ekki annars svæðis til að ákvarða gerð upphæðar sem dreifingin er fyrir.</span><span class="sxs-lookup"><span data-stu-id="11e31-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="11e31-349">Hins vegar **munum** við nota þessar upplýsingar í næstu aðstæðum, þar sem kröfur fyrir þær aðstæður tilgreina að aðrar upphæðagerðir hafi dreifingar (t.d. vsk).</span><span class="sxs-lookup"><span data-stu-id="11e31-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="11e31-350">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="11e31-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="11e31-351">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="11e31-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="11e31-352">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="11e31-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="11e31-353">Eins og er er fartækjasíðan **Skoða bókhald** ekki tengd við neina af þeim fartækjasíðum sem við höfum hannað hingað til.</span><span class="sxs-lookup"><span data-stu-id="11e31-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="11e31-354">Þar sem notandinn ætti að geta flett að síðunni **Skoða bókhald** af síðunni **Upplýsingar um reikning** í fartækinu, verðum við að veita flettingar af síðunni **Upplýsingar um reikning** á síðuna **Skoða bókhald**.</span><span class="sxs-lookup"><span data-stu-id="11e31-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="11e31-355">Við komum þessari flettingu á með því að nota viðbótar rök í gegnum JavaScript.</span><span class="sxs-lookup"><span data-stu-id="11e31-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="11e31-356">Opnaðu .js-skrána sem þú stofnaðir áður og bættu við línum sem eru auðkenndar í eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="11e31-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="11e31-357">Þessi kóði gerir tvennt:</span><span class="sxs-lookup"><span data-stu-id="11e31-357">This code does two things:</span></span>
    1.  <span data-ttu-id="11e31-358">Hann hjálpar við að tryggja að notendur geti ekki farið beint af vinnusvæðinu á síðuna **Skoða bókhald**.</span><span class="sxs-lookup"><span data-stu-id="11e31-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="11e31-359">Hann kemur á flettistýringu af síðunni **Upplýsingar um reikning** á síðuna **Skoða bókhald**.</span><span class="sxs-lookup"><span data-stu-id="11e31-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="11e31-360">Heiti síðnanna og annarra stýringa í kóðanum verða að vera þau sömu og heitin í vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="11e31-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  <span data-ttu-id="11e31-361">Hlaða upp skrá kóða vinnusvæðið með því að velja flipann **Röklegt** til að yfirskrifa fyrri kóða</span><span class="sxs-lookup"><span data-stu-id="11e31-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="11e31-362">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="11e31-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="11e31-363">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="11e31-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="11e31-364">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="11e31-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="11e31-365">Villuleit</span><span class="sxs-lookup"><span data-stu-id="11e31-365">Validation</span></span>

<span data-ttu-id="11e31-366">Opnaðu forritið úr fartækinu og tengdu við tilvikið.</span><span class="sxs-lookup"><span data-stu-id="11e31-366">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="11e31-367">Athugaðu að þú skráir þig inn í fyrirtæki þar sem reikningum lánardrottna eru úthlutuð til þín til skoðunar.</span><span class="sxs-lookup"><span data-stu-id="11e31-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="11e31-368">Þú ættir að geta framkvæmt eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="11e31-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="11e31-369">Sjá vinnusvæðið **Mínar samþykktir**.</span><span class="sxs-lookup"><span data-stu-id="11e31-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="11e31-370">Farðu niður í vinnusvæðið **Mínar samþykktir** og sjáðu síðuna **Mínir reikningar lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="11e31-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="11e31-371">Farðu niður í vinnusvæðið **Mínar samþykktir** og sjáðu lista yfir reikninga sem var úthlutað til þín.</span><span class="sxs-lookup"><span data-stu-id="11e31-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="11e31-372">Kafa í einn af reikningunum og sjá upplýsingar um haus og línuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="11e31-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="11e31-373">Á upplýsingasíðunni sjá tengil við viðhengi og notið þennan tengil til að fara í viðhengjalista og skoða viðhengin.</span><span class="sxs-lookup"><span data-stu-id="11e31-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="11e31-374">Á upplýsingasíðunni sjá tengil við síðuna **Skoða bókhald** og notið þennan tengil til að fara á dreifingasíðuna og skoða dreifingarnar.</span><span class="sxs-lookup"><span data-stu-id="11e31-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="11e31-375">Á upplýsingasíðu, smellið á valmyndina **Aðgerðir** neðst, og framkvæma verkflæðisaðgerðir sem eiga við um skref í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="11e31-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="11e31-376">Hönnun á flóknum aðstæðum reikningssamþykkta fyrir Fabrikam</span><span class="sxs-lookup"><span data-stu-id="11e31-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11e31-377">Sviðsmyndareigind</span><span class="sxs-lookup"><span data-stu-id="11e31-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="11e31-378">Svara</span><span class="sxs-lookup"><span data-stu-id="11e31-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11e31-379">Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="11e31-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="11e31-380">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="11e31-380">Vendor name</span></span></li>
<li><span data-ttu-id="11e31-381">Reikningsupphæð</span><span class="sxs-lookup"><span data-stu-id="11e31-381">Invoice amount</span></span></li>
<li><span data-ttu-id="11e31-382">Reikningslykill</span><span class="sxs-lookup"><span data-stu-id="11e31-382">Invoice account</span></span></li>
<li><span data-ttu-id="11e31-383">Númer reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-383">Invoice number</span></span></li>
<li><span data-ttu-id="11e31-384">Reikningsdagsetning</span><span class="sxs-lookup"><span data-stu-id="11e31-384">Invoice date</span></span></li>
<li><span data-ttu-id="11e31-385">Lýsing reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-385">Invoice description</span></span></li>
<li><span data-ttu-id="11e31-386">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="11e31-386">Due date</span></span></li>
<li><span data-ttu-id="11e31-387">Gjaldmiðill reiknings</span><span class="sxs-lookup"><span data-stu-id="11e31-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e31-388">Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="11e31-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="11e31-389">Innkaupategund</span><span class="sxs-lookup"><span data-stu-id="11e31-389">Procurement category</span></span></li>
<li><span data-ttu-id="11e31-390">Magn</span><span class="sxs-lookup"><span data-stu-id="11e31-390">Quantity</span></span></li>
<li><span data-ttu-id="11e31-391">Einingarverð</span><span class="sxs-lookup"><span data-stu-id="11e31-391">Unit price</span></span></li>
<li><span data-ttu-id="11e31-392">Nettóupphæð línu</span><span class="sxs-lookup"><span data-stu-id="11e31-392">Line net amount</span></span></li>
<li><span data-ttu-id="11e31-393">Upphæð 1099</span><span class="sxs-lookup"><span data-stu-id="11e31-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11e31-394">Hversu margar reikningslínur eru í reikningi?</span><span class="sxs-lookup"><span data-stu-id="11e31-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="11e31-395">Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.</span><span class="sxs-lookup"><span data-stu-id="11e31-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="11e31-396">5</span><span class="sxs-lookup"><span data-stu-id="11e31-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e31-397">Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum?</span><span class="sxs-lookup"><span data-stu-id="11e31-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="11e31-398">Já</span><span class="sxs-lookup"><span data-stu-id="11e31-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11e31-399">Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld og svo framvegis) eru fyrir reikningslínuna?</span><span class="sxs-lookup"><span data-stu-id="11e31-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="11e31-400">Aftur skal nota 80-20 reglu.</span><span class="sxs-lookup"><span data-stu-id="11e31-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="11e31-401">Heildarverð: 2 vsk: 2 Gjöld: 2</span><span class="sxs-lookup"><span data-stu-id="11e31-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11e31-402">Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings?</span><span class="sxs-lookup"><span data-stu-id="11e31-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="11e31-403">Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?</span><span class="sxs-lookup"><span data-stu-id="11e31-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="11e31-404">Ekki notað</span><span class="sxs-lookup"><span data-stu-id="11e31-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11e31-405">Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?</span><span class="sxs-lookup"><span data-stu-id="11e31-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="11e31-406">Já</span><span class="sxs-lookup"><span data-stu-id="11e31-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="11e31-407">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="11e31-407">Next steps</span></span>

<span data-ttu-id="11e31-408">Eftirfarandi frávik er hægt að gera fyrir aðstæður 1, byggt á þörfum fyrir aðstæður 2.</span><span class="sxs-lookup"><span data-stu-id="11e31-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="11e31-409">Þennan hluta má nota til að endurbæta umhverfi fartækjaforrits þíns.</span><span class="sxs-lookup"><span data-stu-id="11e31-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="11e31-410">Þar sem fleiri línur á reikningi eru væntanlegar í dæmi 2, munu eftirfarandi breytingar á hönnuninni aðstoða við fínstillingu á notendaupplifun í fartækinu:</span><span class="sxs-lookup"><span data-stu-id="11e31-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="11e31-411">Í stað þess að skoða reikningslínur á upplýsingasíðu (eins og í dæmi 1), geta notendur valið að skoða línur á sérstakri farsímasíðu.</span><span class="sxs-lookup"><span data-stu-id="11e31-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="11e31-412">Þar sem búist er við fleiri en einni reikningslínu í þessu dæmi, ef síðan **VendMobileInvoiceAllDistributionTree** er notuð til að hanna dreifingarsíðu fyrir fartæki (eins og í dæmi 1), gæti það verið ruglandi fyrir notandann að tengja línur við dreifingar.</span><span class="sxs-lookup"><span data-stu-id="11e31-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="11e31-413">Notið þess vegna síðuna **VendMobileInvoiceLineDistributionTree** til að hanna dreifingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="11e31-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="11e31-414">Góð regla er að dreifing skuli sýnd í samhengi við reikningslínu í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="11e31-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="11e31-415">Þess vegna þarf að tryggja að notandinn geti kafað í línu til að sjá dreifingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="11e31-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="11e31-416">Notaðu tenglagetu síðunnar til að koma á köfun, rétt eins og gert var fyrir haus og upplýsingasíðurnar í dæmi 1.</span><span class="sxs-lookup"><span data-stu-id="11e31-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="11e31-417">Þar sem búist er við fleiri en einni gerð upphæðar í dreifingu í dæmi 2 (vsk, gjöld, og svo framvegis) verður gagnlegt að sýna lýsingu á gerð upphæðar.</span><span class="sxs-lookup"><span data-stu-id="11e31-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="11e31-418">(Þessum upplýsingum var sleppt í dæmi 1.)</span><span class="sxs-lookup"><span data-stu-id="11e31-418">(We omitted this information in scenario 1.)</span></span>




