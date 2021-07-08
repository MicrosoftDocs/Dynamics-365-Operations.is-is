---
title: Nýjungar eða breytingar í farsímaforriti Warehouse Management
description: Í þessu efnisatriði er að finna lista yfir nýja og breytta eiginleika fyrir hverja útgefna útgáfu af farsímaforriti Warehouse Management fyrir Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261782"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="cb6d1-103">Nýjungar eða breytingar í farsímaforriti Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="cb6d1-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb6d1-104">Í þessu efnisatriði er að finna nýja eiginleika, lagfæringar, endurbætur og þekkt vandamál fyrir hverja útgefna útgáfu af farsímaforriti Warehouse Management fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="cb6d1-105">Útgáfa 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="cb6d1-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="cb6d1-106">Nýir eiginleikar, lagfæringar og bætur í útgáfu 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="cb6d1-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="cb6d1-107">Þessi útgáfa kynnir eftirfarandi nýja eiginleika, lagfæringar og endurbætur:</span><span class="sxs-lookup"><span data-stu-id="cb6d1-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="cb6d1-108">Sýnistilling sýnir nú öll merki á tungumáli tækis.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="cb6d1-109">Minni líkur eru á að fá eftirfarandi villuboð: „Ekki er hægt að finna hentugt yfirlit fyrir tilgreinda stærð.“</span><span class="sxs-lookup"><span data-stu-id="cb6d1-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="cb6d1-110">Lágmarkshæð vinnuspjalds hefur verið aukin (í tilvikum þar sem þrír eða færri reitir eru stilltir á að birtast í verkefnalistanum).</span><span class="sxs-lookup"><span data-stu-id="cb6d1-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="cb6d1-111">Spássíur neðst á upplýsingaspjöldum hafa verið endurbættar.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="cb6d1-112">Ógild tákn í XML-skrám sem skipst er á við þjóninn eru nú meðhöndluð á hnökralausan hátt.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="cb6d1-113">(Til dæmis eru stafir sem prentast ekki nú meðhöndlaðir á hnökralausan hátt og leiða ekki lengur til þess að forritið frjósi.)</span><span class="sxs-lookup"><span data-stu-id="cb6d1-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="cb6d1-114">HTTP-villur (eins og „villa 503“) þegar netþjónsbeiðni er send er nú meðhöndlaðar á hnökralausan hátt.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="cb6d1-115">Þó að villa sé sýnd er listinn yfir valmöguleika ekki lengur sýndur sjálfkrafa fyrir stýringar samsettra glugga.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="cb6d1-116">Forritið frýs ekki lengur vegna skjástefnunar sem er valin í notandastillingum.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="cb6d1-117">Myndir afurða eru nú sýndar í sjálfsafgreiðsluumhverfum.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="cb6d1-118">(Þessi breyting á eingöngu við um útgáfur í lágri upplausn.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="cb6d1-119">Þjónusta skráarstjórnunar styður ekki myndir í fullri stærð í sjálfsafgreiðsluumhverfum.)</span><span class="sxs-lookup"><span data-stu-id="cb6d1-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="cb6d1-120">Vandamál varðandi of litla tiltekt upp á núll í magni hefur verið lagað.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="cb6d1-121">Forritið frýs ekki lengur þegar upplýsingaspjald sýnir marga eins reiti.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="cb6d1-122">Þekkt vandamál í útgáfu 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="cb6d1-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="cb6d1-123">Eftirfarandi þekkt vandamál eru til í þessari útgáfu:</span><span class="sxs-lookup"><span data-stu-id="cb6d1-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="cb6d1-124">Með tímanum hægist á forritinu (sérstaklega verkefnalistanum).</span><span class="sxs-lookup"><span data-stu-id="cb6d1-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="cb6d1-125">**Windows-útgáfa:** Þegar USB-skanni er notaður til að skanna í Windows valda ósamkvæmar niðurstöður því að skönnuð tákn blandast saman.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="cb6d1-126">Útgáfa 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="cb6d1-126">Version 2.0.5.0</span></span>

<span data-ttu-id="cb6d1-127">Þessi útgáfa kynnir eftirfarandi nýja eiginleika, lagfæringar og endurbætur:</span><span class="sxs-lookup"><span data-stu-id="cb6d1-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="cb6d1-128">Leyniorð biðlara er ekki lengur falið í uppsetningu tengistillingarinnar.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="cb6d1-129">Nú er hægt að ýta lengi á hvaða texta sem er til að sjá hann til fulls.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="cb6d1-130">Villuboðin þegar vantar geymsluheimildir hafa verið endurbætt.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="cb6d1-131">Nýjum stýringarröðum hefur verið bætt við sum flæðin.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="cb6d1-132">Hnappur innsendingar verður ekki lengur í boði á röngum tímum vegna gluggastærðar.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="cb6d1-133">Sleðar geta nú verið áfram á smærri skjáum þegar stærri hnappastærðir eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="cb6d1-134">Fjögurra hnappa yfirlögnin er ekki lengur klippt burt.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="cb6d1-135">Lyklaborðið styður nú hnapp eyðingar.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="cb6d1-136">Leyst hefur verið úr birtuvandamáli sem gæti komið upp þegar ýtt er á lyklaborðið.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="cb6d1-137">Búið er að laga ýmis vandamál varðandi sýnigögn.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="cb6d1-138">Leyst hefur verið úr vandamáli sem hafði áhrif á talnareiti á upplýsingasíðunni.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="cb6d1-139">Skjályklaborðið hverfur ekki lengur af og til á sumum tækjum.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="cb6d1-140">Ýmsar villur í notendaviðmóti hafa verið lagfærðar, svo sem villur sem höfðu áhrif á bakgrunnslit og staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="cb6d1-141">Rússneska í viðmótinu hefur verið bætt.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="cb6d1-142">Ýmis vandamál sem ollu því að kerfið fraus hafa verið löguð.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="cb6d1-143">Leyst hefur verið úr vandamáli sem tengdist enduropnun reiknivélarinnar.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="cb6d1-144">**Android útgáfa:** Leyst hefur verið úr vandamáli sem leiddi til þess að Android 4.4 fraus við ræsingu.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="cb6d1-145">**Android útgáfa:** Lágmarksskölun hefur verið minnkuð um 50 prósent.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="cb6d1-146">Útgáfa 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="cb6d1-146">Version 2.0.4.0</span></span>

<span data-ttu-id="cb6d1-147">Útgáfa 2.0.4.0 var fyrsta almenna útgáfan sem var í boði í farsímaforriti Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="cb6d1-148">Nýir eiginleikar, lagfæringar og bætur í útgáfu 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="cb6d1-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="cb6d1-149">Þessi útgáfa kynnir eftirfarandi nýja eiginleika, lagfæringar og endurbætur sem voru ekki í boði í forútgáfunni:</span><span class="sxs-lookup"><span data-stu-id="cb6d1-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="cb6d1-150">Ef upplýsingaspjald inniheldur tvö merki sem eru með eins gögn verður eitt merkið falið.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="cb6d1-151">Sérstafir eru nú sjálfgefið sýndir og valkosturinn til að fela þá hefur verið fjarlægður úr notandastillingum.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="cb6d1-152">Óvirkir innsendingarhnappar eru nú sýndir ótiltækir í smækkuðu yfirliti.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="cb6d1-153">Breyting á rökum röðunar fyrir stýringar tryggja hnökralausa skölun milli tækja.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="cb6d1-154">Þar af leiðandi er minni þörf á að laga skölun leturgerða eða hnappa.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="cb6d1-155">Sjálfgefna litaþemanu hefur verið breytt í *Dökkt*.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="cb6d1-156">Táknið sem vantar fyrir óvirkan innsendingarhnapp hefur verið bætt við borðayfirlitið.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="cb6d1-157">Undanþágur vegna tímalokunar fara nú með notanda yfir á tengingarsíðuna í stað þess að sýna villu í línunni.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="cb6d1-158">Ef engin innsendingaraðgerð er í boði (t.d. **Í lagi**, **Já**, **Samþykkja**, **Búið** eða **Lokið**) verður innsendingarhnappurinn gerður óvirkur.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="cb6d1-159">Stöðugleiki forrits hefur verið bættur.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-159">App stability has been improved.</span></span>
- <span data-ttu-id="cb6d1-160">Komin er lagfæring á veikleika öryggis [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="cb6d1-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="cb6d1-161">**Windows-útgáfa:** Vandamál í Windows þar sem valmyndir svöruðu ekki eftir að stærð glugga var breytt hefur verið lagað.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="cb6d1-162">Þekkt vandamál í útgáfu 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="cb6d1-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="cb6d1-163">Eftirfarandi þekkt vandamál er til staðar í þessari útgáfu:</span><span class="sxs-lookup"><span data-stu-id="cb6d1-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="cb6d1-164">Vandamál kom upp í þessari útgáfu með tæki sem notar Android 4.4.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="cb6d1-165">Þú gætir lent í vandamálum þegar forritið er notað í þessari Android-útgáfu.</span><span class="sxs-lookup"><span data-stu-id="cb6d1-165">You might experience issues when you use the app on this Android version.</span></span>
