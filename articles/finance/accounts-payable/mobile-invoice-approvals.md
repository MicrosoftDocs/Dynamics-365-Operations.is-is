---
title: Reikningssamþykktir í fartækjum
description: Í þessu efnisatriði er ætlað að gefa praktíska nálgun til að hanna farsímaaðstæður með því að taka reikningssamþykktir fyrir fartæki sem notkunartilvik.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5d3b85e076292b9d41de6a4cf3198ed9b38d27c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828035"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="eb3e6-103">Reikningssamþykktir í fartækjum</span><span class="sxs-lookup"><span data-stu-id="eb3e6-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb3e6-104">Farsímageta gerir fyrirtækjanotenda kleift að hanna farsímaupplifun.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="eb3e6-105">Fyrir ítarlegri dæmi leyfir kerfið forriturum einnig að framlengja getu eins og þeir vilja.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="eb3e6-106">Skilvirkasta leiðin til að læra sum af nýju hugtökunum í fartæki er að fara gegnum ferlið að hanna ný dæmi.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="eb3e6-107">Í þessu efnisatriði er ætlað að gefa praktíska nálgun til að hanna farsímaaðstæður með því að taka reikningssamþykktir fyrir fartæki sem notkunartilvik.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="eb3e6-108">Þetta efnisatriði á að aðstoða við hönnun á öðrum frávikum á aðstæðum og einnig er hægt að nota það í öðrum aðstæðum sem eru ekki eru tengdar reikningum lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="eb3e6-109">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="eb3e6-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="eb3e6-110">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="eb3e6-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="eb3e6-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="eb3e6-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3e6-112">Fyrirframlestur farsímahandbókar</span><span class="sxs-lookup"><span data-stu-id="eb3e6-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="eb3e6-113">Fartækjaverkvangur</span><span class="sxs-lookup"><span data-stu-id="eb3e6-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="eb3e6-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="eb3e6-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="eb3e6-115">Vertu viss um að þú sért að nota umhverfi sem er með útgáfu 1611 og uppfærslu verkvangs 3 (nóvember 2016).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="eb3e6-116">Setja upp bráðabót KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="eb3e6-117">Verkskráning getur skráð rangt tvær Loka skipanir fyrir felliglugga; þetta er innifalið í uppfærslu verkvangs 3 (uppfærsla nóvember 2016).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="eb3e6-118">Setja upp bráðabót KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="eb3e6-119">Þessi bráðabót leyfir að viðhengi séu skoðuð í farsímabiðlara; þetta er innifalið í uppfærslu verkvangs 3 (uppfærsla í nóvember 2016).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="eb3e6-120">Setja upp bráðabót KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="eb3e6-121">Forritakóði fyrir farsímasamþykkt reiknings lánardrottins; þetta er innifalið í útgáfu 7.0.1 (maí 2016).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="eb3e6-122">Í tæki með Android eða iOS eða Windows sem er með farsímaforritið sem er uppsett.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="eb3e6-123">Leita að forritinu í viðeigandi forritaverslun.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="eb3e6-124">Inngangur</span><span class="sxs-lookup"><span data-stu-id="eb3e6-124">Introduction</span></span>
<span data-ttu-id="eb3e6-125">Farsímasamþykktir fyrir reikninga lánardrottins þurfa þrjár bráðabætur sem nefndar eru í hlutanum „Forkröfur“.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="eb3e6-126">Þessar bráðabætur veita ekki vinnusvæði fyrir reikningssamþykki.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="eb3e6-127">Til að læra hvað vinnusvæði er í samhengi við fartæki, skaltu lesa farsímahandbókina sem er nefnd í hlutanum „Forkröfur“.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="eb3e6-128">Vinnusvæði reikningssamþykkta verður að vera hannað.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="eb3e6-129">Hvert fyrirtæki skipuleggur og skilgreinir mismunandi viðskiptaferli fyrir reikninga lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="eb3e6-130">Áður en farsímaupplifun fyrir samþykktir reiknings lánardrottins er hönnuð ætti að íhuga að eftirfarandi þætti viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="eb3e6-131">Hugmyndin er að nota þessa gagnapunkta eins mikið og hægt er til að hámarka reynslu notanda á tækinu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="eb3e6-132">Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="eb3e6-133">Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="eb3e6-134">Hversu margar reikningslínur eru í reikningi?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="eb3e6-135">Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="eb3e6-136">Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="eb3e6-137">Ef svarið þessari spurningu er já, íhugið eftirfarandi spurningar:</span><span class="sxs-lookup"><span data-stu-id="eb3e6-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="eb3e6-138">Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld, skipti og svo framvegis) eru fyrir reikningslínu?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="eb3e6-139">Aftur skal nota 80-20 reglu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="eb3e6-140">Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="eb3e6-141">Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="eb3e6-142">Þetta efnisatriði útskýrir ekki hvernig á að breyta dreifingu fjárhagsupphæða þar sem þessi virkni er ekki studd eins og stendur fyrir farsímaaðstæður.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="eb3e6-143">Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="eb3e6-144">Hönnun farsímareynslu fyrir reikningssamþykktir verður mismunandi, eftir því hver svörin verða við þessum spurningum.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="eb3e6-145">Markmiðið er að fínstilla reynslu notanda fyrir viðskiptaferli í fartæki innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="eb3e6-146">Í afganginum af þessu efnisatriði skoðum við tvær frávikaaðstæður sem byggjast á mismunandi svörum við spurningunum hér á undan.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="eb3e6-147">Almennt séð, þegar unnið er með farsímahönnuði, þarf að ganga úr skugga um að 'birta' breytingarnar til að koma í veg fyrir uppfærslur mistakist.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="eb3e6-148">Hönnun á einföldum aðstæðum reikningssamþykktar fyrir Contoso</span><span class="sxs-lookup"><span data-stu-id="eb3e6-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb3e6-149">Sviðsmyndareigind</span><span class="sxs-lookup"><span data-stu-id="eb3e6-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="eb3e6-150">Svara</span><span class="sxs-lookup"><span data-stu-id="eb3e6-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb3e6-151">Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="eb3e6-152">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="eb3e6-152">Vendor name</span></span></li>
<li><span data-ttu-id="eb3e6-153">Heildarupphæð reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-153">Invoice total</span></span></li>
<li><span data-ttu-id="eb3e6-154">Reikningslykill</span><span class="sxs-lookup"><span data-stu-id="eb3e6-154">Invoice account</span></span></li>
<li><span data-ttu-id="eb3e6-155">Númer reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-155">Invoice number</span></span></li>
<li><span data-ttu-id="eb3e6-156">Reikningsdagsetning</span><span class="sxs-lookup"><span data-stu-id="eb3e6-156">Invoice date</span></span></li>
<li><span data-ttu-id="eb3e6-157">Lýsing reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-157">Invoice description</span></span></li>
<li><span data-ttu-id="eb3e6-158">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="eb3e6-158">Due date</span></span></li>
<li><span data-ttu-id="eb3e6-159">Gjaldmiðill reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e6-160">Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="eb3e6-161">Innkaupategund</span><span class="sxs-lookup"><span data-stu-id="eb3e6-161">Procurement category</span></span></li>
<li><span data-ttu-id="eb3e6-162">Magn</span><span class="sxs-lookup"><span data-stu-id="eb3e6-162">Quantity</span></span></li>
<li><span data-ttu-id="eb3e6-163">Einingarverð</span><span class="sxs-lookup"><span data-stu-id="eb3e6-163">Unit price</span></span></li>
<li><span data-ttu-id="eb3e6-164">Nettóupphæð línu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-164">Line net amount</span></span></li>
<li><span data-ttu-id="eb3e6-165">Upphæð 1099</span><span class="sxs-lookup"><span data-stu-id="eb3e6-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e6-166">Hversu margar reikningslínur eru í reikningi?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="eb3e6-167">Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="eb3e6-168">1</span><span class="sxs-lookup"><span data-stu-id="eb3e6-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e6-169">Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="eb3e6-170">Já</span><span class="sxs-lookup"><span data-stu-id="eb3e6-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e6-171">Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld og svo framvegis) eru fyrir reikningslínuna?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="eb3e6-172">Aftur skal nota 80-20 reglu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="eb3e6-173">Heildarverð: 2 vsk: 0 Gjöld: 0</span><span class="sxs-lookup"><span data-stu-id="eb3e6-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e6-174">Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="eb3e6-175">Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="eb3e6-176">Ekki notað</span><span class="sxs-lookup"><span data-stu-id="eb3e6-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e6-177">Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="eb3e6-178">Já</span><span class="sxs-lookup"><span data-stu-id="eb3e6-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="eb3e6-179">Stofna vinnusvæðið</span><span class="sxs-lookup"><span data-stu-id="eb3e6-179">Create the workspace</span></span>

1.  <span data-ttu-id="eb3e6-180">Í vafra og skráðu þig inn í forritið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="eb3e6-181">Eftir að notandi hefur verið skráður bæta **&mode = fartæki** vefslóð eins og sýnt er í eftirfarandi dæmi og endurnýja þarf síðuna: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="eb3e6-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="eb3e6-182">Smellið á hnappinn **Stillingar** (tannhjól) í efst til hægri á síðunni og smelltu svo á **Fartæki forrits**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="eb3e6-183">Hönnuður fartæki forrits verður birtast eins og Verkskráning birtist.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="eb3e6-184">Smelltu á **Bæta við** til að búa til nýtt vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="eb3e6-185">Í þessu dæmi er vinnusvæðinu gefið heitið **Samþykktir**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="eb3e6-186">Færðu inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-186">Enter a description.</span></span>
6.  <span data-ttu-id="eb3e6-187">Velja lit vinnusvæðis</span><span class="sxs-lookup"><span data-stu-id="eb3e6-187">Select a workspace color.</span></span> <span data-ttu-id="eb3e6-188">Litur vinnusvæðisins verður notaður fyrir heildarstíl fyrir farsímareynslu fyrir þetta vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="eb3e6-189">Velja tákn fyrir vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="eb3e6-190">Smelltu á **Lokið**</span><span class="sxs-lookup"><span data-stu-id="eb3e6-190">Click **Done**</span></span>
9.  <span data-ttu-id="eb3e6-191">Smelltu á **Birta vinnusvæði** til að vista breytingarnar</span><span class="sxs-lookup"><span data-stu-id="eb3e6-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="eb3e6-192">Reikningar lánardrottins tengdir notanda</span><span class="sxs-lookup"><span data-stu-id="eb3e6-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="eb3e6-193">Fyrsta farsímasíðan sem ætti að hanna er listi yfir reikninga sem eru úthlutaðir notandanum til skoðunar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="eb3e6-194">Til að hanna þessa farsímasíðu notarðu síðuna **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="eb3e6-195">Áður en lokið er við þetta ferli skal ganga úr skugga um að a.m.k. einn lánardrottinsreikningur sé úthlutaður til þín til skoðunar og að reikningslínan hafi tvær dreifingar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="eb3e6-196">Þessi uppsetning uppfyllir kröfur fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="eb3e6-197">Í vefslóðinni skal skipta út heiti valmyndaratriðis með **VendMobileInvoiceAssignedToMeListPage** til að opna farsímaútgáfu af listasíðunni **Biðreikningar lánardrottins sem mér eru úthlutaðir** í kerfiseiningunni **Viðskiptaskuldir**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="eb3e6-198">Það fer eftir fjölda reikninga sem er úthlutað til þín í kerfinu en þessi síða sýnir þá reikninga.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="eb3e6-199">Til að finna tilgreindan reikning er hægt að nota síuna til vinstri.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="eb3e6-200">Hins vegar þurfum við ekki tilgreindan reikning fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="eb3e6-201">Við þurfum bara reikning sem úthlutað er til þín, sem gerir þér kleift að hanna farsímasíðuna.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="eb3e6-202">Nýjar síður sem eru tiltækar hafa verið hannaðar sérstaklega fyrir þróun farsímaaðstæðna fyrir reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="eb3e6-203">Þess vegna verður að nota þessar síður.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="eb3e6-204">Vefslóðin á að líkjast eftirfarandi vefslóð og þegar hún hefur verið færð inn verður síðan sem er sýnd á skýringarmyndinni að birtast: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="eb3e6-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="eb3e6-205">[![Síðan Reikningar lánardrottins í bið sem notanda hefur verið úthlutað](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="eb3e6-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="eb3e6-206">Smellið á hnappinn **Stillingar** (tannhjól) í efra hægra horni síðunnar og svo á **Farsímaforrit**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="eb3e6-207">Veljið vinnustöð og smellið á **Breyta**</span><span class="sxs-lookup"><span data-stu-id="eb3e6-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="eb3e6-208">Smellið á **Bæta við síðu** til að stofna fyrstu farsímasíðuna.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="eb3e6-209">Færið inn heiti, eins og **Mínar lánardrottnareikningar**, og lýsingu, eins og **Reikninga lánardrottins sem mér eru úthlutaðir til skoðunar**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="eb3e6-210">Smelltu á **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-210">Click **Done**.</span></span>
7.  <span data-ttu-id="eb3e6-211">Í farsímahönnuði, á flipanum **Svæði** er smellt á **Velja svæði**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="eb3e6-212">Dálkar á listasíðunni verða að líkjast eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="eb3e6-213">[![Dálkar á síðunni Reikningar lánardrottins í bið sem notanda hefur verið úthlutað](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="eb3e6-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="eb3e6-214">Bæta þarf dálkum af listasíðunni, sem verða að birtast notendum á farsímasíðunni.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="eb3e6-215">Röðin sem þú bætir við er sú röð sem svæðin eru birt notanda.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="eb3e6-216">Eina leiðin til að breyta röðun svæða verður með því að velja aftur öll svæði.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="eb3e6-217">Samkvæmt kröfum fyrir þetta dæmi er eftirfarandi átta svæða krafist.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="eb3e6-218">Hins vegar gæti sumum notendum þótt átta svæði of mikið af upplýsingum til að hafa í farsíma.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="eb3e6-219">Þess vegna munum við aðeins sýna mikilvægustu svæðin í farsímalistayfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="eb3e6-220">Eftirstandandi svæði birtast í upplýsingayfirliti sem við munum hanna seinna.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="eb3e6-221">Eins og stendur bætum við eftirfarandi svæðum við.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-221">For now, we will add the following fields.</span></span> <span data-ttu-id="eb3e6-222">Smellið á plúsmerkið (**+**) í þessum dálkum til að bæta við farsíðu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="eb3e6-223">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="eb3e6-223">Vendor name</span></span>
    - <span data-ttu-id="eb3e6-224">Heildarupphæð reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-224">Invoice total</span></span>
    - <span data-ttu-id="eb3e6-225">Reikningslykill</span><span class="sxs-lookup"><span data-stu-id="eb3e6-225">Invoice account</span></span>
    - <span data-ttu-id="eb3e6-226">Númer reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-226">Invoice number</span></span>
    - <span data-ttu-id="eb3e6-227">Reikningsdagsetning</span><span class="sxs-lookup"><span data-stu-id="eb3e6-227">Invoice date</span></span>

    <span data-ttu-id="eb3e6-228">Eftir að svæðum er bætt við síðuna verður farsímasíðan að líkjast eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="eb3e6-229">[![Síðan eftir að svæðum hefur verið bætt við](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="eb3e6-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="eb3e6-230">Einnig verður að bæta eftirfarandi dálkum við núna, svo að við getum virkjað verkflæðisaðgerðir síðar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="eb3e6-231">Sýna lokin verk</span><span class="sxs-lookup"><span data-stu-id="eb3e6-231">Show complete task</span></span>
    - <span data-ttu-id="eb3e6-232">Sýna úthlutað verk</span><span class="sxs-lookup"><span data-stu-id="eb3e6-232">Show delegate task</span></span>
    - <span data-ttu-id="eb3e6-233">Sýna afturkallað verk</span><span class="sxs-lookup"><span data-stu-id="eb3e6-233">Show recall task</span></span>
    - <span data-ttu-id="eb3e6-234">Sýna hafnað verk</span><span class="sxs-lookup"><span data-stu-id="eb3e6-234">Show reject task</span></span>
    - <span data-ttu-id="eb3e6-235">Sýna verk með umbeðin lok</span><span class="sxs-lookup"><span data-stu-id="eb3e6-235">Show request completion task</span></span>
    - <span data-ttu-id="eb3e6-236">Sýna endursent verk</span><span class="sxs-lookup"><span data-stu-id="eb3e6-236">Show resubmit task</span></span>

10. <span data-ttu-id="eb3e6-237">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="eb3e6-238">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="eb3e6-239">Smelltu á **Birta vinnusvæði** til að vista verkið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="eb3e6-240">Virkja **Birta samtölu á biðstöðu lánardrottins reiknings reikninga lista** í færibreytuskjámynd viðskiptaskulda undir **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="eb3e6-241">Athugið að aðeins með því að virkja þessa færibreytu verða reikningssamtölur reiknaðar til að birtast á listasíðu lánardrottnareikninga í bið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="eb3e6-242">Þetta er ný geta sem er hluti af frumskilyrðum bráðabóta 3208224.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="eb3e6-243">Reikningsupplýsingar lánardrottins</span><span class="sxs-lookup"><span data-stu-id="eb3e6-243">Vendor invoice details</span></span>

<span data-ttu-id="eb3e6-244">Til að hanna reikningsupplýsingasíðu fyrir farsíma skal nota síðuna **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="eb3e6-245">Athugið að það fer eftir fjölda reikninga sem er úthlutað til þín í kerfinu en þessi síða sýnir elsta reikninginn (reikninginn sem var stofnaður fyrst).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="eb3e6-246">Til að finna tilgreindan reikning er hægt að nota síuna til vinstri.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="eb3e6-247">Hins vegar þurfum við ekki tilgreindan reikning fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="eb3e6-248">Við þurfum bara reikningsgögn svo að við getum hannað farsímasíðuna.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="eb3e6-249">[![Verkflæðissíða](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="eb3e6-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="eb3e6-250">Í vefslóðinni skal skipta út heiti valmyndaratriðis með **VendMobileInvoiceHeaderDetails** til að opna skjámyndina</span><span class="sxs-lookup"><span data-stu-id="eb3e6-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="eb3e6-251">Opnið hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="eb3e6-252">Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="eb3e6-253">Veldu síðuna **Reikningar lánardrottna minna** sem þú bjóst til áður og smelltu síðan á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="eb3e6-254">Á flipanum **Svæði** smellirðu á dálkhausinn **Hnitanet**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="eb3e6-255">Smellið á **Eiginleikar &gt; Bæta við síðu**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="eb3e6-256">**Athugasemd:** Þegar smellt er á fyrirsögnina **Hnitanet** og síðu bætt við, er venslum við upplýsingasíðu sjálfvirkt komið á.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="eb3e6-257">Færðu inn síðutitill, eins og **Upplýsingar um reikning**, og lýsingu, eins og **Skoða línuupplýsingar og reikningshausinn**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="eb3e6-258">Smellið á **Velja svæði**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-258">Click **Select fields**.</span></span> <span data-ttu-id="eb3e6-259">Athugið að röðin sem þú bætir við er sú röð sem svæðin verða birt notanda.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="eb3e6-260">Eina leiðin til að breyta röðun svæða verður með því að velja aftur öll svæði.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="eb3e6-261">Bættu við eftirfarandi reitum úr haus, samkvæmt kröfum fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="eb3e6-262">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="eb3e6-262">Vendor name</span></span>
   - <span data-ttu-id="eb3e6-263">Heildarupphæð reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-263">Invoice total</span></span>
   - <span data-ttu-id="eb3e6-264">Reikningslykill</span><span class="sxs-lookup"><span data-stu-id="eb3e6-264">Invoice account</span></span>
   - <span data-ttu-id="eb3e6-265">Númer reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-265">Invoice number</span></span>
   - <span data-ttu-id="eb3e6-266">Reikningsdagsetning</span><span class="sxs-lookup"><span data-stu-id="eb3e6-266">Invoice date</span></span>
   - <span data-ttu-id="eb3e6-267">Lýsing reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-267">Invoice description</span></span>
   - <span data-ttu-id="eb3e6-268">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="eb3e6-268">Due date</span></span>
   - <span data-ttu-id="eb3e6-269">Gjaldmiðill reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-269">Invoice currency</span></span>

10. <span data-ttu-id="eb3e6-270">Bæta við eftirfarandi svæðum úr línutöflunni á síðuna:</span><span class="sxs-lookup"><span data-stu-id="eb3e6-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="eb3e6-271">Innkaupategund</span><span class="sxs-lookup"><span data-stu-id="eb3e6-271">Procurement category</span></span>
    - <span data-ttu-id="eb3e6-272">Magn</span><span class="sxs-lookup"><span data-stu-id="eb3e6-272">Quantity</span></span>
    - <span data-ttu-id="eb3e6-273">Einingarverð</span><span class="sxs-lookup"><span data-stu-id="eb3e6-273">Unit price</span></span>
    - <span data-ttu-id="eb3e6-274">Nettóupphæð línu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-274">Line net amount</span></span>
    - <span data-ttu-id="eb3e6-275">Upphæð 1099</span><span class="sxs-lookup"><span data-stu-id="eb3e6-275">1099 amount</span></span>

11. <span data-ttu-id="eb3e6-276">Eftir að öllum svæðum úr fyrri tvö skref hefur verið bætt við, smellið á **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="eb3e6-277">Dálkar á listasíðunni verða að líkjast eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="eb3e6-278">[![Síðan eftir að svæðum hefur verið bætt við](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="eb3e6-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="eb3e6-279">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="eb3e6-280">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="eb3e6-281">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="eb3e6-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="eb3e6-282">Verkflæðisaðgerðir</span><span class="sxs-lookup"><span data-stu-id="eb3e6-282">Workflow actions</span></span>

<span data-ttu-id="eb3e6-283">Til að bæta við verkflæðisaðgerðum skal nota síðuna **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="eb3e6-284">Til að opna þessa síðu skal skipta út heiti valmyndaratriðis í vefslóð, eins og gert var áður.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="eb3e6-285">Síðan skal opna hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="eb3e6-286">Fylgið þessum skrefum til að bæta við verkflæðisaðgerðum á upplýsingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="eb3e6-287">Þú verður að hafa reikninga úthlutaða þér með rétta stöðu svo að verkflæðisaðgerðir sem þú ætlar að hanna fyrir séu tiltækar þér.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="eb3e6-288">Skráning verkflæðisaðgerða</span><span class="sxs-lookup"><span data-stu-id="eb3e6-288">Record workflow actions</span></span>
1.  <span data-ttu-id="eb3e6-289">Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="eb3e6-290">Veldu síðuna **Upplýsingar um reikning** sem þú stofnaðir áður og smelltu síðan á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="eb3e6-291">Á flipanum **Aðgerðir** er smellt á **Bæta aðgerð við**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="eb3e6-292">Færðu inn aðgerðatitill eins og **Samþykkja**, og lýsingu, eins og **Samþykkja reikninginn**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="eb3e6-293">Athugið að titill aðgerðarinnar sem er færður hér inn verður heiti aðgerðarinnar sem er birt notanda í farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="eb3e6-294">Smelltu á **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-294">Click **Done**.</span></span>
6.  <span data-ttu-id="eb3e6-295">Smellið á **Velja svæði**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="eb3e6-296">Fara í gegnum verkflæðisferlið í **VendMobileInvoiceHeaderDetails** síðunni og ljúka við aðgerðina sem óskað er að skrá.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="eb3e6-297">Gangið úr skugga um að færa inn athugasemdir um verkflæðið meðan á því stendur þannig að athugasemdasvæðið sé einnig innifalið í farsímareynslunni.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="eb3e6-298">Þegar aðgerð verkflæðis hefur verið keyrð er smellt á **Gert** að ljúka verkinu fyrir Valið svæði.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="eb3e6-299">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="eb3e6-300">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="eb3e6-301">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="eb3e6-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="eb3e6-302">Endurtaktu fyrra skref til að skrá allar nauðsynlegar verkflæðisaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="eb3e6-303">Stofnaðu .js-skrá</span><span class="sxs-lookup"><span data-stu-id="eb3e6-303">Create a .js file</span></span>
1. <span data-ttu-id="eb3e6-304">Opna Notepad eða Microsoft Visual Studio og líma eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="eb3e6-305">Vista skýrsluna sem .js-skrá</span><span class="sxs-lookup"><span data-stu-id="eb3e6-305">Save the file as a .js file.</span></span> <span data-ttu-id="eb3e6-306">Þessi kóði gerir eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="eb3e6-306">This code does the following:</span></span>
    - <span data-ttu-id="eb3e6-307">Hann felur aukalega dálka sem tengjast verkflæði, sem við bættum við áður á fartæki listasíðu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="eb3e6-308">Við bættum þessum dálkum við svo að forritið hafi upplýsingar í samhengi og geti framkvæmt næsta skref.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="eb3e6-309">Á grunni verkflæðisskrefsins sem er virkt notar það rök til að sýna aðeins þær aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eb3e6-310">Heiti síðnanna og annarra stýringa í kóðanum verða að vera þau sömu og heitin í vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
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
    ```

2.  <span data-ttu-id="eb3e6-311">Hlaða upp kóðaskrá á vinnusvæðið með því að velja flipann **Röklegt**</span><span class="sxs-lookup"><span data-stu-id="eb3e6-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="eb3e6-312">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="eb3e6-313">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="eb3e6-314">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="eb3e6-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="eb3e6-315">Viðhengi reiknings lánardrottins</span><span class="sxs-lookup"><span data-stu-id="eb3e6-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="eb3e6-316">Smellið á hnappinn **Stillingar** (tannhjól) í efra hægra horni síðunnar og svo á **Farsímaforrit**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="eb3e6-317">Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="eb3e6-318">Veldu <strong>\*\*Síðuna Reikningsupplýsingar sem þú stofnaðir áður áðan og smelltu síðan \*\*Breyta</strong>.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="eb3e6-319">Stilltu valkostinn **Skjalastjórnun** á **Já** eins og sýnt er hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="eb3e6-320">**Athugasemd:** Ef ekki þarf að sýna viðhengi í fartækinu er hægt að hafa þennan valkost stilltan á **Nei**, sem er sjálfgefin stilling.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Skjalastjórnun](./media/docmanagement-216x300.png)

5. <span data-ttu-id="eb3e6-322">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="eb3e6-323">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="eb3e6-324">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="eb3e6-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="eb3e6-325">Línudreifingar fyrir reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="eb3e6-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="eb3e6-326">Kröfur fyrir þetta dæmi staðfesta að það verða aðeins dreifingar á línustigi dreifingar og að reikningur verður alltaf með aðeins eina línu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="eb3e6-327">Þar sem þessar aðstæður eru einfaldar verður notendaupplifunin í fartækinu einnig að vera nógu einföld til að notandinn þurfi ekki að kafa niður nokkrum þrep til að skoða dreifingu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="eb3e6-328">Lánardrottnareikningar hafa þann valkost að sýna alla skiptingu úr haus reiknings.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="eb3e6-329">Þessi reynsla er það sem þarf fyrir farsímaaðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="eb3e6-330">Þess vegna munum við nota síðuna **VendMobileInvoiceAllDistributionTree** til að hanna þennan hluta farsímaaðstæðnanna.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="eb3e6-331">Þegar við þekkjum kröfurnar hjálpar það okkur að ákveða hvaða tiltekna síðu á að nota og hvernig á að fínstilla notandaupplifun farsíma nákvæmlega þegar við hönnum aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="eb3e6-332">Í seinni aðstæðunum munum við nota aðra síðu til að sýna dreifingarnar, þar sem kröfur fyrir þær aðstæður eru aðrar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="eb3e6-333">Í vefslóðinni skiptirðu út heiti valmyndaratriðis, eins og þú gerðir áður.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="eb3e6-334">Síðan sem birtist á líkjast eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="eb3e6-335">[![Síðan Allar dreifingar](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="eb3e6-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="eb3e6-336">Opnið hönnuðinn fartæki með hnappninum **Stillingar** (tannhjól).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="eb3e6-337">Smellið á **Breyta** hnappinn til að hefja breytingarham í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="eb3e6-338">**Athugasemd:** Þú munt sjá að tvær nýjar síður voru sjálfkrafa stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="eb3e6-339">Kerfið stofnar þessar síður þar sem kveikt var á skjalastjórnun í fyrri hluta.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="eb3e6-340">Þú mátt hunsa þessi nýjar síður.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="eb3e6-341">Smella á **Bæta við síðu**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="eb3e6-342">Færa inn síðutitill, eins og **Skoða bókhald**, og lýsingu, eins og **Skoða bókhald fyrir reikning**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="eb3e6-343">Smelltu á **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-343">Click **Done**.</span></span>

7.  <span data-ttu-id="eb3e6-344">Á flipanum **Svæði** er smellt á **Velja svæði**, veljið eftirfarandi svæði af dreifingasíðunni og smellið síðan á **Gert**:</span><span class="sxs-lookup"><span data-stu-id="eb3e6-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="eb3e6-345">Upphæð</span><span class="sxs-lookup"><span data-stu-id="eb3e6-345">Amount</span></span>
    2.  <span data-ttu-id="eb3e6-346">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="eb3e6-346">Currency</span></span>
    3.  <span data-ttu-id="eb3e6-347">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="eb3e6-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="eb3e6-348">Við völdum ekki dálkinn **Lýsing** dálkur úr hnitaneti dreifinga, þar sem kröfur fyrir aðstæðurnar staðfestu að heildarverð er aðeins upphæðin sem dreifingar verða að vera fyrir.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="eb3e6-349">Þess vegna krefst notandi ekki annars svæðis til að ákvarða gerð upphæðar sem dreifingin er fyrir.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="eb3e6-350">Hins vegar **munum** við nota þessar upplýsingar í næstu aðstæðum, þar sem kröfur fyrir þær aðstæður tilgreina að aðrar upphæðagerðir hafi dreifingar (t.d. vsk).</span><span class="sxs-lookup"><span data-stu-id="eb3e6-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="eb3e6-351">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="eb3e6-352">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="eb3e6-353">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="eb3e6-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="eb3e6-354">Leiðsögn bætt við síðuna „Skoða bókhald“</span><span class="sxs-lookup"><span data-stu-id="eb3e6-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="eb3e6-355">Eins og er er fartækjasíðan **Skoða bókhald** ekki tengd við neina af þeim fartækjasíðum sem við höfum hannað hingað til.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="eb3e6-356">Þar sem notandinn ætti að geta flett að síðunni **Skoða bókhald** af síðunni **Upplýsingar um reikning** í fartækinu, verðum við að veita flettingar af síðunni **Upplýsingar um reikning** á síðuna **Skoða bókhald**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="eb3e6-357">Við komum þessari flettingu á með því að nota viðbótar rök í gegnum JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="eb3e6-358">Opnaðu .js-skrána sem þú stofnaðir áður og bættu við línum sem eru auðkenndar í eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="eb3e6-359">Þessi kóði gerir tvennt:</span><span class="sxs-lookup"><span data-stu-id="eb3e6-359">This code does two things:</span></span>
    1.  <span data-ttu-id="eb3e6-360">Hann hjálpar við að tryggja að notendur geti ekki farið beint af vinnusvæðinu á síðuna **Skoða bókhald**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="eb3e6-361">Hann kemur á flettistýringu af síðunni **Upplýsingar um reikning** á síðuna **Skoða bókhald**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="eb3e6-362">Heiti síðnanna og annarra stýringa í kóðanum verða að vera þau sömu og heitin í vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
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
    ```
    
2.  <span data-ttu-id="eb3e6-363">Hlaða upp skrá kóða vinnusvæðið með því að velja flipann **Röklegt** til að yfirskrifa fyrri kóða</span><span class="sxs-lookup"><span data-stu-id="eb3e6-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="eb3e6-364">Smellið á **Lokið** til að fara úr breytingarstillinigu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="eb3e6-365">Smellið á **Til baka** og síðan **Lokið** til að fara af vinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="eb3e6-366">Smelltu á **Birta vinnusvæði** til að vista verkið</span><span class="sxs-lookup"><span data-stu-id="eb3e6-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="eb3e6-367">Villuleit</span><span class="sxs-lookup"><span data-stu-id="eb3e6-367">Validation</span></span>

<span data-ttu-id="eb3e6-368">Opnaðu forritið úr fartækinu og tengdu við tilvikið.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="eb3e6-369">Athugaðu að þú skráir þig inn í fyrirtæki þar sem reikningum lánardrottna eru úthlutuð til þín til skoðunar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="eb3e6-370">Þú ættir að geta framkvæmt eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="eb3e6-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="eb3e6-371">Sjá vinnusvæðið **Mínar samþykktir**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="eb3e6-372">Farðu niður í vinnusvæðið **Mínar samþykktir** og sjáðu síðuna **Mínir reikningar lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="eb3e6-373">Farðu niður í vinnusvæðið **Mínar samþykktir** og sjáðu lista yfir reikninga sem var úthlutað til þín.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="eb3e6-374">Kafa í einn af reikningunum og sjá upplýsingar um haus og línuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="eb3e6-375">Á upplýsingasíðunni sjá tengil við viðhengi og notið þennan tengil til að fara í viðhengjalista og skoða viðhengin.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="eb3e6-376">Á upplýsingasíðunni sjá tengil við síðuna **Skoða bókhald** og notið þennan tengil til að fara á dreifingasíðuna og skoða dreifingarnar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="eb3e6-377">Á upplýsingasíðu, smellið á valmyndina **Aðgerðir** neðst, og framkvæma verkflæðisaðgerðir sem eiga við um skref í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="eb3e6-378">Hönnun á flóknum aðstæðum reikningssamþykkta fyrir Fabrikam</span><span class="sxs-lookup"><span data-stu-id="eb3e6-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb3e6-379">Sviðsmyndareigind</span><span class="sxs-lookup"><span data-stu-id="eb3e6-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="eb3e6-380">Svara</span><span class="sxs-lookup"><span data-stu-id="eb3e6-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb3e6-381">Hvaða svæði úr reikningsfyrirsögninni mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="eb3e6-382">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="eb3e6-382">Vendor name</span></span></li>
<li><span data-ttu-id="eb3e6-383">Reikningsupphæð</span><span class="sxs-lookup"><span data-stu-id="eb3e6-383">Invoice amount</span></span></li>
<li><span data-ttu-id="eb3e6-384">Reikningslykill</span><span class="sxs-lookup"><span data-stu-id="eb3e6-384">Invoice account</span></span></li>
<li><span data-ttu-id="eb3e6-385">Númer reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-385">Invoice number</span></span></li>
<li><span data-ttu-id="eb3e6-386">Reikningsdagsetning</span><span class="sxs-lookup"><span data-stu-id="eb3e6-386">Invoice date</span></span></li>
<li><span data-ttu-id="eb3e6-387">Lýsing reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-387">Invoice description</span></span></li>
<li><span data-ttu-id="eb3e6-388">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="eb3e6-388">Due date</span></span></li>
<li><span data-ttu-id="eb3e6-389">Gjaldmiðill reiknings</span><span class="sxs-lookup"><span data-stu-id="eb3e6-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e6-390">Hvaða svæði úr reikningslínunum mun notandi vilja sjá í farsímareynslunni og í hvaða pöntun?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="eb3e6-391">Innkaupategund</span><span class="sxs-lookup"><span data-stu-id="eb3e6-391">Procurement category</span></span></li>
<li><span data-ttu-id="eb3e6-392">Magn</span><span class="sxs-lookup"><span data-stu-id="eb3e6-392">Quantity</span></span></li>
<li><span data-ttu-id="eb3e6-393">Einingarverð</span><span class="sxs-lookup"><span data-stu-id="eb3e6-393">Unit price</span></span></li>
<li><span data-ttu-id="eb3e6-394">Nettóupphæð línu</span><span class="sxs-lookup"><span data-stu-id="eb3e6-394">Line net amount</span></span></li>
<li><span data-ttu-id="eb3e6-395">Upphæð 1099</span><span class="sxs-lookup"><span data-stu-id="eb3e6-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e6-396">Hversu margar reikningslínur eru í reikningi?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="eb3e6-397">Nota reglu 80-20 hér og fínstilla fyrir 80 prósent.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="eb3e6-398">5</span><span class="sxs-lookup"><span data-stu-id="eb3e6-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e6-399">Munu notendur vilja sjá dreifingar á fjárhagsupphæð (reikningskóðun) í fartækinu við skoðunarferlum?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="eb3e6-400">Já</span><span class="sxs-lookup"><span data-stu-id="eb3e6-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e6-401">Hversu margar dreifingar á fjárhagsupphæð (heildarverð, vsk, gjöld og svo framvegis) eru fyrir reikningslínuna?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="eb3e6-402">Aftur skal nota 80-20 reglu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="eb3e6-403">Heildarverð: 2 vsk: 2 Gjöld: 2</span><span class="sxs-lookup"><span data-stu-id="eb3e6-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb3e6-404">Eru reikningarnir einnig með dreifingu fjárhagsupphæða í haus reiknings?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="eb3e6-405">Ef svo er, ættu þessar dreifingar á fjárhagsupphæð að vera tiltækar í tækinu?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="eb3e6-406">Ekki notað</span><span class="sxs-lookup"><span data-stu-id="eb3e6-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb3e6-407">Munu notendur vilja sjá viðhengi fyrir reikninginn í tækinu?</span><span class="sxs-lookup"><span data-stu-id="eb3e6-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="eb3e6-408">Já</span><span class="sxs-lookup"><span data-stu-id="eb3e6-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="eb3e6-409">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="eb3e6-409">Next steps</span></span>

<span data-ttu-id="eb3e6-410">Eftirfarandi frávik er hægt að gera fyrir aðstæður 1, byggt á þörfum fyrir aðstæður 2.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="eb3e6-411">Þennan hluta má nota til að endurbæta umhverfi fartækjaforrits þíns.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="eb3e6-412">Þar sem fleiri línur á reikningi eru væntanlegar í dæmi 2, munu eftirfarandi breytingar á hönnuninni aðstoða við fínstillingu á notendaupplifun í fartækinu:</span><span class="sxs-lookup"><span data-stu-id="eb3e6-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="eb3e6-413">Í stað þess að skoða reikningslínur á upplýsingasíðu (eins og í dæmi 1), geta notendur valið að skoða línur á sérstakri farsímasíðu.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="eb3e6-414">Þar sem búist er við fleiri en einni reikningslínu í þessu dæmi, ef síðan **VendMobileInvoiceAllDistributionTree** er notuð til að hanna dreifingarsíðu fyrir fartæki (eins og í dæmi 1), gæti það verið ruglandi fyrir notandann að tengja línur við dreifingar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="eb3e6-415">Notið þess vegna síðuna **VendMobileInvoiceLineDistributionTree** til að hanna dreifingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="eb3e6-416">Góð regla er að dreifing skuli sýnd í samhengi við reikningslínu í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="eb3e6-417">Þess vegna þarf að tryggja að notandinn geti kafað í línu til að sjá dreifingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="eb3e6-418">Notaðu tenglagetu síðunnar til að koma á köfun, rétt eins og gert var fyrir haus og upplýsingasíðurnar í dæmi 1.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="eb3e6-419">Þar sem búist er við fleiri en einni gerð upphæðar í dreifingu í dæmi 2 (vsk, gjöld, og svo framvegis) verður gagnlegt að sýna lýsingu á gerð upphæðar.</span><span class="sxs-lookup"><span data-stu-id="eb3e6-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="eb3e6-420">(Þessum upplýsingum var sleppt í dæmi 1.)</span><span class="sxs-lookup"><span data-stu-id="eb3e6-420">(We omitted this information in scenario 1.)</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]