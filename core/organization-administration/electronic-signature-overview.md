---
title: "Yfirlit yfir rafrænar undirskriftir"
description: "Þessi grein gefur yfirlit yfir rafrænar undirskriftir og lýsir hvernig hægt er að nota þær í Microsoft Dynamics 365 for Finance and Operations."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e81d4a29cf1624619c1f0c2bfc6bc66c715a6b7f
ms.openlocfilehash: fa3aff17f3f55cdee9abf1f0326ac2bbe599bf94
ms.contentlocale: is-is
ms.lasthandoff: 08/24/2017

---

# <a name="electronic-signature-overview"></a><span data-ttu-id="911f5-103">Yfirlit yfir rafrænar undirskriftir</span><span class="sxs-lookup"><span data-stu-id="911f5-103">Electronic signature overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="911f5-104">Þessi grein gefur yfirlit yfir rafrænar undirskriftir og lýsir hvernig hægt er að nota þær í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="911f5-104">This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-an-electronic-signature"></a><span data-ttu-id="911f5-105">Hvað er rafræn undirskrift?</span><span class="sxs-lookup"><span data-stu-id="911f5-105">What is an electronic signature?</span></span>
--------------------------------

<span data-ttu-id="911f5-106">Rafræn undirskrift staðfestir deili á þeim aðila sem er í þann mund að hefja eða samþykkja ferli.</span><span class="sxs-lookup"><span data-stu-id="911f5-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="911f5-107">Innan sumra atvinnugreina er rafræn undirskrift jafn bindandi að lögum og handskrifuð.</span><span class="sxs-lookup"><span data-stu-id="911f5-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> 

<span data-ttu-id="911f5-108">Reglur kveða á um rafrænar undirskriftir innan ýmissa atvinnugreina sem eru háðar opinberum reglugerðum, svo sem við lyfja-, matvæla- og drykkjarvöruframleiðslu og í flugvéla- og geimiðnaði og varnariðnaði.</span><span class="sxs-lookup"><span data-stu-id="911f5-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="911f5-109">Þær eru einnig nauðsynlegar samkvæmt reglum 21 CFR hluta 11, sem gefnar eru út af Matvæla- og lyfjaeftirliti Bandaríkjanna (FDA).</span><span class="sxs-lookup"><span data-stu-id="911f5-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span> 

<span data-ttu-id="911f5-110">**Athugið:** Rafræn undirskrift er ekki það sama og stafræn undirskrift.</span><span class="sxs-lookup"><span data-stu-id="911f5-110">**Note:** An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="911f5-111">Rafræn undirskrift er aðeins staðgengill handskrifaðra undirskrifta, en stafrænar undirskriftir hafa ítarlegri öryggiseiginleika.</span><span class="sxs-lookup"><span data-stu-id="911f5-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="911f5-112">Með stafrænum undirskriftum er hægt að kanna hvort notandi eða vinnsla hafi átt við gögn.</span><span class="sxs-lookup"><span data-stu-id="911f5-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="911f5-113">Einnig er hægt að staðfesta stafrænar undirskriftir án þess að eigandi skírteinis sem var notað til undirskriftar geti þráttað fyrir það.</span><span class="sxs-lookup"><span data-stu-id="911f5-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="911f5-114">Rafrænar undirskriftir í Microsoft Dynamics 365 for Finance and Operations eru með innbyggða virkni stafrænnar undirskriftum, eins og lýst er hér fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="911f5-114">As described below, electronic signatures in Microsoft Dynamics 365 for Finance and Operations have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="911f5-115">Rafrænar undirskriftir í Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="911f5-115">Electronic signatures in Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="911f5-116">Hægt er að nota rafrænar undirskriftir fyrir mikilvæg viðskiptaferli í Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="911f5-116">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="911f5-117">Rafrænar undirskriftir eru innbyggður hluti sumra ferla.</span><span class="sxs-lookup"><span data-stu-id="911f5-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="911f5-118">Hægt er að búa til kröfur um rafrænar undirskriftir fyrir hvaða gagnagrunn eða svæði sem er.</span><span class="sxs-lookup"><span data-stu-id="911f5-118">You can also create custom signature requirements for any database table and field.</span></span> 

<span data-ttu-id="911f5-119">Rafrænar undirskriftir deila nokkrum eiginleikum með stafrænum undirskriftum.</span><span class="sxs-lookup"><span data-stu-id="911f5-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="911f5-120">Allir notendur sem skrifa undir skjöl þurfa að hafa gilt dulritað skírteini.</span><span class="sxs-lookup"><span data-stu-id="911f5-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="911f5-121">Þegar skjal er undirritað er einkalykillinn sem tengist skírteininu sannprófaður.</span><span class="sxs-lookup"><span data-stu-id="911f5-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="911f5-122">Finance and Operations skráir upplýsingar um rafrænar undirskriftir í kladda til þess að hægt sé að rekja slóð aðgerða.</span><span class="sxs-lookup"><span data-stu-id="911f5-122">Finance and Operations records electronic signature information in a log to provide an audit trail.</span></span> <span data-ttu-id="911f5-123">Setja upp rafrænar undirskriftir, sjá [Uppsetning rafrænna undirskrifta (verkefnaleiðbeiningar)](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-up-electronic-signatures).</span><span class="sxs-lookup"><span data-stu-id="911f5-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-up-electronic-signatures).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="911f5-124">Notendur sem þarfnast aðgangs að rafrænar undirskriftir</span><span class="sxs-lookup"><span data-stu-id="911f5-124">Users who require access to electronic signatures</span></span>
<span data-ttu-id="911f5-125">Þrenns konar notendur krefjast vanalega öryggisaðgangs að rafrænum undirskriftum: Stjórnendur rafrænna undirskrifta, áritendur og endurskoðendur rafrænna undirskrifta.</span><span class="sxs-lookup"><span data-stu-id="911f5-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="911f5-126">Stjórnandi rafrænna undirskrifta</span><span class="sxs-lookup"><span data-stu-id="911f5-126">Electronic signature administrator</span></span>

<span data-ttu-id="911f5-127">Stjórnandi rafrænna undirskrifta setur upp kröfur um rafrænar undirskriftir, almennar færibreytur og samþykkjendur og fær viðvörum um það þegar sannvottun undirskriftar mistekst.</span><span class="sxs-lookup"><span data-stu-id="911f5-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="911f5-128">Sjálfgefið er að notendur sem tilheyra öryggishlutverki **upplýsingatæknistjóra** hafi heimild til að stjórna rafrænum undirskriftum.</span><span class="sxs-lookup"><span data-stu-id="911f5-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="911f5-129">Áritari</span><span class="sxs-lookup"><span data-stu-id="911f5-129">Signer</span></span>

<span data-ttu-id="911f5-130">Áritari skrifar undir skjöl og ferli sem þarfnast undirskrifta.</span><span class="sxs-lookup"><span data-stu-id="911f5-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="911f5-131">Sjálfgefið er að notendur sem tilheyra öryggishlutverki **Kerfisnotandi** hafi heimild til undirrita skjöl rafrænt.</span><span class="sxs-lookup"><span data-stu-id="911f5-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span> 

<span data-ttu-id="911f5-132">**Athugasemd** Áritari kann að þurfa viðbótarheimildir til að fá aðgang að gögnum sem tengjast skjölum eða ferlum sem er skrifað undir.</span><span class="sxs-lookup"><span data-stu-id="911f5-132">**Note:** The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="911f5-133">Notendur sem gera breytingar á gögnum og þurfa að skrifa undir þær verða að hafa heimildir til að breyta gögnunum.</span><span class="sxs-lookup"><span data-stu-id="911f5-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="911f5-134">Notandi sem skrifar undir fyrir hönd annars notanda gæti ekki þurft aðgang að gögnunum.</span><span class="sxs-lookup"><span data-stu-id="911f5-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="911f5-135">Dæmi af þessari gerð notanda er yfirmaður sem skrifar undir fyrir breytingar starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="911f5-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="911f5-136">Endurskoðandi rafrænna undirskrifta</span><span class="sxs-lookup"><span data-stu-id="911f5-136">Electronic signature auditor</span></span>

<span data-ttu-id="911f5-137">Endurskoðandi rafrænna undirskrifta skoðar kladda gagnagrunns og kladda undirskrifta sem er aðgengilegur úr kladda gagnagrunnsins.</span><span class="sxs-lookup"><span data-stu-id="911f5-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="911f5-138">Sjálfgefið er að notendur sem tilheyra öryggishlutverki **upplýsingatæknistjóra** hafi heimild til að endurskoða rafrænum undirskriftum.</span><span class="sxs-lookup"><span data-stu-id="911f5-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span> 

<span data-ttu-id="911f5-139">Ef notað er hlutverk annað en **upplýsingatæknistjóri** skal ganga úr skugga um að hlutverki er úthlutað eftirfarandi réttindum:</span><span class="sxs-lookup"><span data-stu-id="911f5-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

-   <span data-ttu-id="911f5-140">Skoða mistök rafrænna undirskrifta</span><span class="sxs-lookup"><span data-stu-id="911f5-140">View electronic signature failures</span></span>
-   <span data-ttu-id="911f5-141">Skoða gagnagrunnskladda</span><span class="sxs-lookup"><span data-stu-id="911f5-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="911f5-142">Rafræn undirskrift skjals</span><span class="sxs-lookup"><span data-stu-id="911f5-142">Signing documents electronically</span></span>
### <a name="get-a-certificate"></a><span data-ttu-id="911f5-143">Sækja skírteini</span><span class="sxs-lookup"><span data-stu-id="911f5-143">Get a certificate</span></span>

<span data-ttu-id="911f5-144">Áður en skjöl eru undirrituð rafrænt í Dynamics 365 for Finance and Operations þarf að biðja um skírteini.</span><span class="sxs-lookup"><span data-stu-id="911f5-144">Before you sign documents electronically in Finance and Operations, you must request a certificate.</span></span> 

<span data-ttu-id="911f5-145">**Athugið:** Finance and Operations notar aðgerðir Microsoft SQL Server til að stofna skírteini og virkja rafræna undirritun.</span><span class="sxs-lookup"><span data-stu-id="911f5-145">**Note:** Finance and Operations uses Microsoft SQL Server features to create certificates and enable electronic signing.</span></span> <span data-ttu-id="911f5-146">Ekki þarf að hafa annað umhverfi fyrir skírteini eða lykla.</span><span class="sxs-lookup"><span data-stu-id="911f5-146">No additional certificate or public key infrastructure (PKI) is required.</span></span> 

<span data-ttu-id="911f5-147">Þegar þú biður um skírteini eru opinn lykill og einkalykill stofnaðir fyrir þig í gagnagrunni Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="911f5-147">When you request a certificate, a public key and a private key are created for you in the Finance and Operations database.</span></span> <span data-ttu-id="911f5-148">Einkalykillinn er dulritaður með aðgangsorði sem aðeins þú veist hvað er.</span><span class="sxs-lookup"><span data-stu-id="911f5-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="911f5-149">Þegar þú undirritar skjöl rafrænt er auðkenni þitt sannprófað þegar þú færir inn aðgangsorðið.</span><span class="sxs-lookup"><span data-stu-id="911f5-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span> 

<span data-ttu-id="911f5-150">Til að biðja um skírteini, á **Valkosti** síðunni á **Lykla** flipanum, smellið **Fá skírteini**.</span><span class="sxs-lookup"><span data-stu-id="911f5-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span> 

<span data-ttu-id="911f5-151">Þú þarft að slá inn og staðfestu aðgangsorðið sem þú notar vegna undirskrifta.</span><span class="sxs-lookup"><span data-stu-id="911f5-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="911f5-152">Aðgangsorðið er notað til að verja lykilinn þinn og heimila notkun skírteinisins.</span><span class="sxs-lookup"><span data-stu-id="911f5-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="911f5-153">Aðgangsorðið er ekki vistað í gagnagrunninum og er ekki aðgengilegt öðrum, þ.m.t. kerfisstjóra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="911f5-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the Finance and Operations administrator.</span></span> 

<span data-ttu-id="911f5-154">Ef þú manst ekki aðgangsorðið sem þarf til að tengjast skírteininu þarf að endurstilla skírteinið.</span><span class="sxs-lookup"><span data-stu-id="911f5-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="911f5-155">Endurstilling þess hefur ekki áhrif á skjöl sem þú hefur undirritað með því.</span><span class="sxs-lookup"><span data-stu-id="911f5-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="911f5-156">Til að endurstilla skírteinið, á **Valkosti** síðunni er smellt á **Endurstilla skírteini**.</span><span class="sxs-lookup"><span data-stu-id="911f5-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="911f5-157">Rafræn undirskrift skjals</span><span class="sxs-lookup"><span data-stu-id="911f5-157">Sign a document electronically</span></span>

<span data-ttu-id="911f5-158">Síðan **Skrifa undir skjal** birtist þegar breyting er gerð sem krefst rafrænnar undirskriftar.</span><span class="sxs-lookup"><span data-stu-id="911f5-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1.  <span data-ttu-id="911f5-159">Á **Skrifa undir skjal** síðunni smellirðu á **Skjal** til að skoða breytingar sem voru gerðar á skjalinu.</span><span class="sxs-lookup"><span data-stu-id="911f5-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2.  <span data-ttu-id="911f5-160">Veldu ástæðukóða á flipanum **Undirskrift**.</span><span class="sxs-lookup"><span data-stu-id="911f5-160">On the **Signature** tab, select a reason code.</span></span>
3.  <span data-ttu-id="911f5-161">Færið inn athugasemd ef athugasemd er krafist.</span><span class="sxs-lookup"><span data-stu-id="911f5-161">Enter a comment, if a comment is required.</span></span>
4.  <span data-ttu-id="911f5-162">Ef notandakennið þitt birtist ekki á svæðinu **Áritari** skaltu velja það af listanum.</span><span class="sxs-lookup"><span data-stu-id="911f5-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5.  <span data-ttu-id="911f5-163">Færið inn staðsetningu þína, ef þörf er á þessum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="911f5-163">Enter your location, if this information is required.</span></span>
6.  <span data-ttu-id="911f5-164">Smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="911f5-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="911f5-165">Skrifa undir fyrir breytingar annars notanda</span><span class="sxs-lookup"><span data-stu-id="911f5-165">Sign for another user's changes</span></span>

<span data-ttu-id="911f5-166">Stundum þarf notandi að skrifa undir fyrir breytingar annars notanda.</span><span class="sxs-lookup"><span data-stu-id="911f5-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="911f5-167">Til dæmis gæti stjórnandi þurft að skrifa undir breytingar sem starfsmaður gerir á uppskrift.</span><span class="sxs-lookup"><span data-stu-id="911f5-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="911f5-168">Notaðu þetta ferli til að gera notanda Finance and Operations að áritara fyrir annan notanda.</span><span class="sxs-lookup"><span data-stu-id="911f5-168">Use this procedure to designate a Finance and Operations user as a signer for another user.</span></span> 

<span data-ttu-id="911f5-169">**Athugið:** Þegar notandi skrifar undir fyrir breytingar annars notanda verður undirskriftin að vera veitt á vinnustöð notandans sem gerði breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="911f5-169">**Note:** When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="911f5-170">Notandinn getur ekki vistað breytinguna fyrr en undirskrift hefur verið innt af hendi.</span><span class="sxs-lookup"><span data-stu-id="911f5-170">The user can't save the change until the signature has been provided.</span></span> 

<span data-ttu-id="911f5-171">Fylgið eftirfarandi skrefum til að tilgreina samþykkjendur.</span><span class="sxs-lookup"><span data-stu-id="911f5-171">To designate approvers, follow these steps.</span></span>

1.  <span data-ttu-id="911f5-172">Á síðunni **Valkosti** á flipanum **Lykla**, smellið **Tilgreina samþykkjanda**.</span><span class="sxs-lookup"><span data-stu-id="911f5-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2.  <span data-ttu-id="911f5-173">Í **notandakenni samþykktaraðila** reit, velja kenni þess notanda sem á að skrifa undir breytingar annars notanda.</span><span class="sxs-lookup"><span data-stu-id="911f5-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3.  <span data-ttu-id="911f5-174">Í **undirrita fyrir notandakenni** reit, velja kenni notandans sem þarf að skrifa undir fyrir þegar hann gerir breytingar.</span><span class="sxs-lookup"><span data-stu-id="911f5-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>





