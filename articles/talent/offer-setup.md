---
title: Setja upp stjórnun tilboða
description: Þetta efni lýsir því hvernig á að setja upp tilboð í Talent.
author: josaw
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43cf13d96e345747e06541267d820e17de7c1763
ms.sourcegitcommit: ea17d2e35c24a141c20ab429897eebf9fa186f61
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/26/2019
ms.locfileid: "768883"
---
# <a name="set-up-offer-management"></a><span data-ttu-id="b61df-103">Setja upp stjórnun tilboða</span><span class="sxs-lookup"><span data-stu-id="b61df-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="b61df-104">Þegar umsækjandi er fluttur í tilboðsstigið í Dynamics 365 for Talent: Attract þarftu að tryggja að hægt sé að búa til tilboð fyrir umsækjandann á fljótlegan hátt, þau samþykkt eftir þörfum og send út til umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="b61df-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="b61df-105">Vegna þess að flest tilboð eru staðlað getur það verið búið til úr endurnýtanlegum sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="b61df-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="b61df-106">Í Attract, eru öll tilboð rúllað í tilboðspakka, sem er safn af einni eða fleiri tilboðsskjölum.</span><span class="sxs-lookup"><span data-stu-id="b61df-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="b61df-107">Í þessu efni er listi yfir öll þau skref sem stjórnandi Attract myndi fylgja til að setja upp mismunandi tilboðspakki sniðmát sem hluta af tilboðsstjórnunargetu í Attract.</span><span class="sxs-lookup"><span data-stu-id="b61df-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="b61df-108">Notendur sem ekki hafa stjórnandi hlutverk hafa ekki aðgang að þessum möguleikum.</span><span class="sxs-lookup"><span data-stu-id="b61df-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="b61df-109">Tilboðsstjórnunarmöguleikar eru tiltækar sem hluti af biðbót við alhliða ráðningar.</span><span class="sxs-lookup"><span data-stu-id="b61df-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="b61df-110">Tilboðsgögn</span><span class="sxs-lookup"><span data-stu-id="b61df-110">Offer data</span></span> 

<span data-ttu-id="b61df-111">Tilboðsgögn eru minnstu einingin innan sniðmáts tilboðspakkans.</span><span class="sxs-lookup"><span data-stu-id="b61df-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="b61df-112">Dæmigerð tilboð samanstendur af venjulegu texta og gildasafni.</span><span class="sxs-lookup"><span data-stu-id="b61df-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="b61df-113">Gildissviðin eru þau eina sem geta breyst á milli tilboðanna.</span><span class="sxs-lookup"><span data-stu-id="b61df-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="b61df-114">Á meðan tilboðssköpunin stendur er mikilvægasti þáttur sem stofnandi tilboðs getur lagt áherslu á, að listinn yfir staðgengla tilboðsgagna sem eru til staðar í sniðmáti tilboðspakka.</span><span class="sxs-lookup"><span data-stu-id="b61df-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="b61df-115">Til að setja upp tilboðsgögn skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="b61df-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="b61df-116">Farðu í **Stjórnun tilboða**.</span><span class="sxs-lookup"><span data-stu-id="b61df-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="b61df-117">Stækkaðu **Safnið** í vinstra yfirlitssvæðinu og farðu síðan á **Tilboðsgögn**.</span><span class="sxs-lookup"><span data-stu-id="b61df-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="b61df-118">Á **Tilboðsgögn** síðunni eru **Upplýsingar umsækjanda** og **Upplýsingar um starf** kafla.</span><span class="sxs-lookup"><span data-stu-id="b61df-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="b61df-119">Attract veitir nokkra tilbúna staðgengla tilboðsgagna.</span><span class="sxs-lookup"><span data-stu-id="b61df-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="b61df-120">Það eru köflum á síðunni til að skipuleggja mismunandi staðgengla tilboðsgagna saman í rökréttum hópum.</span><span class="sxs-lookup"><span data-stu-id="b61df-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="b61df-121">Þessar köflum geta hjálpað við viðhald á tilboðsgögnum og keyrslu gagna á meðan stofnun tilboða stendur.</span><span class="sxs-lookup"><span data-stu-id="b61df-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="b61df-122">Til að búa til nýjan tilboðsgagnahluta skaltu smella á **Bæta við hluta** og slá inn einkvæmt heiti fyrir hlutann.</span><span class="sxs-lookup"><span data-stu-id="b61df-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="b61df-123">Til að bæta staðgenglum tilboðsgagna við hvaða hluta sem er skaltu smella á **Bæta við tilboðsgögnum** og sláðu inn einkvæmt heiti fyrir staðgengilinn.</span><span class="sxs-lookup"><span data-stu-id="b61df-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="b61df-124">Til að breyta heiti hvaða hluta, settu bendilinn yfir heiti hlutans og uppfæra heitið.</span><span class="sxs-lookup"><span data-stu-id="b61df-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="b61df-125">Til að breyta nafni fyrirliggjandi staðgengla tilboðsgagna, skaltu fyrst ganga úr skugga um að staðgengillinn sé ekki hluti af sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="b61df-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="b61df-126">Settu bendilinn yfir staðgengil tilboðsgagnanna og uppfærðu nafnið eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b61df-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="b61df-127">Til að eyða núverandi staðgengli tilboðsgagna skaltu fyrst ganga úr skugga um að staðgengillinn sé ekki hluti af öðru sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="b61df-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="b61df-128">Þá skaltu setja bendilinn yfir staðsetninguna og þegar ruslakörfutáknið birtist skaltu smella á ruslakörfuna staðgengli tilboðsgagnanna.</span><span class="sxs-lookup"><span data-stu-id="b61df-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="b61df-129">Þú getur séð hversu mörg sniðmát staðgengill tilboðsgagna er hluti af númervísinum við hliðina á hverja tilboðsgögn.</span><span class="sxs-lookup"><span data-stu-id="b61df-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="b61df-130">Til að eyða einhverjum hluta skaltu setja bendilinn yfir heitið.</span><span class="sxs-lookup"><span data-stu-id="b61df-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="b61df-131">Ef ekkert af staðgenglum tilboðsgagnanna í hlutanum birtist í hvaða sniðmáti sem er, getur þú smellt á ruslakörfutáknið til að eyða því.</span><span class="sxs-lookup"><span data-stu-id="b61df-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="b61df-132">Ef þú eyðir hlutanum mun einnig eyða öllum staðgenglum tilboðsgagnanna í þessum hluta.</span><span class="sxs-lookup"><span data-stu-id="b61df-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="b61df-133">Eftir að staðgenglar tilboðsgagnanna hafa verið settir upp, geturðu notað þau yfir hvaða sniðmát skjals sem er.</span><span class="sxs-lookup"><span data-stu-id="b61df-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="b61df-134">Staðgenglar tilboðsgagna eru ekki bundin við tiltekið sniðmát - sama sett er hægt að nota á öllum sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="b61df-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="b61df-135">Reglur um tilboðsgögn</span><span class="sxs-lookup"><span data-stu-id="b61df-135">Offer data rules</span></span>

<span data-ttu-id="b61df-136">Flest fyrirtæki hafa reglur um hvernig tilboð verða að vera gerð.</span><span class="sxs-lookup"><span data-stu-id="b61df-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="b61df-137">Til dæmis getur fyrirtækið krafist þess að samsetning hámarkslaun á ársgrundvelli fyrir tiltekna stað og starfsaldursstig verði að vera innan ákveðins sviðs eða að aðeins fáir tiltekin gildi séu mögulegar fyrir tilboðsstig fyrir nýja starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="b61df-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="b61df-138">Attract styður nú allar slíkar gagnareglur með CSV-skrá.</span><span class="sxs-lookup"><span data-stu-id="b61df-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="b61df-139">Til að undirbúa gagnareglur CSV skrá skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="b61df-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="b61df-140">Ákveðið tilboðsgögn fyrir reglussettið.</span><span class="sxs-lookup"><span data-stu-id="b61df-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="b61df-141">Til dæmis, **Árslaun**.</span><span class="sxs-lookup"><span data-stu-id="b61df-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="b61df-142">Tilgreindu háð staðgengilsgildi tilboðsgagna.</span><span class="sxs-lookup"><span data-stu-id="b61df-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="b61df-143">Til dæmis, **Staðsetning starfs** og **Stig**.</span><span class="sxs-lookup"><span data-stu-id="b61df-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="b61df-144">Tilgreindu dálka 1 og 2 sem **Staðsetning starfs** og **Stig**.</span><span class="sxs-lookup"><span data-stu-id="b61df-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="b61df-145">Til að hlaða inn sviðsgildi, veldu dálka 3 og 4 **Árslaun**.</span><span class="sxs-lookup"><span data-stu-id="b61df-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="b61df-146">Til að hlaða upp tilteknu gildi í staðinn fyrir svið, veldu aðeins dálk 3 **Árslaun**.</span><span class="sxs-lookup"><span data-stu-id="b61df-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="b61df-147">Fylltu út Microsoft Excel skrána út frá nauðsynlegum hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="b61df-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="b61df-148">Gakktu úr skugga um að hver röð sé einstök blanda af öllum gildum sem settar eru saman.</span><span class="sxs-lookup"><span data-stu-id="b61df-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="b61df-149">Vista skrána sem CSV sniði.</span><span class="sxs-lookup"><span data-stu-id="b61df-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="b61df-150">Til að hlaða upp regluskrá tilboðsgagnanna skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="b61df-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="b61df-151">Farðu í **Stjórnun tilboða**.</span><span class="sxs-lookup"><span data-stu-id="b61df-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="b61df-152">Stækkaðu **Safnið** hlutann í vinstra yfirlitssvæðinu og farðu síðan á **Reglur tilboðsgagna**.</span><span class="sxs-lookup"><span data-stu-id="b61df-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="b61df-153">Smelltu á **Nýtt gagnasafn** til að birta **Hlaða upp** valmyndina.</span><span class="sxs-lookup"><span data-stu-id="b61df-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="b61df-154">Tilgreinið einkvæmt heiti fyrir reglusettið og hladdu síðan upp vistað CSV skrá.</span><span class="sxs-lookup"><span data-stu-id="b61df-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="b61df-155">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b61df-155">Click **Add**.</span></span>
    <span data-ttu-id="b61df-156">Reglusettið verður unnin í bakgrunni og þú verður tilkynnt í forritinu og í tölvupósti þegar það er lokið.</span><span class="sxs-lookup"><span data-stu-id="b61df-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="b61df-157">Þú verður tilkynnt ef það eru villur meðan þú vinnur með upphleðslu.</span><span class="sxs-lookup"><span data-stu-id="b61df-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="b61df-158">Þú getur síðan sótt villukladdann, lagaðu skrána og hlaðið henni aftur upp.</span><span class="sxs-lookup"><span data-stu-id="b61df-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="b61df-159">Notaðu þrípunktahnappinn (**...**) valkostinn ef þú vilt hlaða niður reglusettinu og uppfæra gildasafnið.</span><span class="sxs-lookup"><span data-stu-id="b61df-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="b61df-160">Eftir uppfærslu geturðu hlaðið skránni aftur upp.</span><span class="sxs-lookup"><span data-stu-id="b61df-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="b61df-161">Þú getur eytt núverandi reglusetti ef staðsetningin sem er skilgreind er ekki notuð í öðru sniðmáti skjals.</span><span class="sxs-lookup"><span data-stu-id="b61df-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="b61df-162">Hver staðgengill getur aðeins haft eitt einstakt sett af dálkum sem það er háð.</span><span class="sxs-lookup"><span data-stu-id="b61df-162">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="b61df-163">Til dæmis, ef **Árslaun** er háð **Staðsetning starfs** og **Stig**, getur þú ekki hlaðið inn öðru reglusetti þar sem **Árslaun** er háð mismunandi settum dálkum.</span><span class="sxs-lookup"><span data-stu-id="b61df-163">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="b61df-164">Þú getur sótt sýnishorn af reglusettum tilboðsgagna á flipanum **Sýnishorn** á **Reglur um tilboðsgögn** síðu.</span><span class="sxs-lookup"><span data-stu-id="b61df-164">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="b61df-165">Þegar stofnandi tilboðs hnekkir gildum sem mælt er með í reglum um tilboðsgögn, er tilboðið merkt sem óhefðbundið og skipað verður samþykki fyrir vinnuflæði.</span><span class="sxs-lookup"><span data-stu-id="b61df-165">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="b61df-166">Sniðmát skjals</span><span class="sxs-lookup"><span data-stu-id="b61df-166">Document templates</span></span>

<span data-ttu-id="b61df-167">Sniðmát tilboðsskjals getur hjálpað stjórnendum að búa til tilboðsbréf.</span><span class="sxs-lookup"><span data-stu-id="b61df-167">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="b61df-168">Sniðmát tilboðsskjals er sambland af textanum sem verður hluti af tilboðinu ásamt skilgreindum staðgenglum tilboðsgagna.</span><span class="sxs-lookup"><span data-stu-id="b61df-168">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="b61df-169">Til að búa til sniðmát tilboðsskjals skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="b61df-169">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="b61df-170">Farðu í **Stjórnun tilboða**.</span><span class="sxs-lookup"><span data-stu-id="b61df-170">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="b61df-171">Stækkaðu **Safnið** í vinstra yfirlitssvæðinu og farðu síðan á **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="b61df-171">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="b61df-172">**Sniðmát** síðunni birtir lista yfir sniðmát skjala sem þegar hafa verið skilgreind.</span><span class="sxs-lookup"><span data-stu-id="b61df-172">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="b61df-173">Til að búa til nýtt sniðmát skjals skaltu smella á **Nýtt sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="b61df-173">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="b61df-174">Sláðu inn einkvæma heitið fyrir sniðmátið og smelltu **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="b61df-174">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="b61df-175">Notaðu textaritil fyrir sniðinn texta til að setja inn eða breyta innihaldi tilboðsskjalsins.</span><span class="sxs-lookup"><span data-stu-id="b61df-175">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="b61df-176">Þú getur sett inn töflur, myndir og tengla með því að nota valkostina sem eru í boði efst á textaritlinum.</span><span class="sxs-lookup"><span data-stu-id="b61df-176">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="b61df-177">Þú getur sett inn staðgengla tilboðsgagna í tilboðsskjalinu með:</span><span class="sxs-lookup"><span data-stu-id="b61df-177">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="b61df-178">Dragðu og slepptu frá hægri glugganum.</span><span class="sxs-lookup"><span data-stu-id="b61df-178">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="b61df-179">Festir staðgengil tilboðsgagna beint á sinn stað.</span><span class="sxs-lookup"><span data-stu-id="b61df-179">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="b61df-180">Sláðu inn **\#** og byrjaðu síðan að slá inn heiti staðgengils tilboðsgagna.</span><span class="sxs-lookup"><span data-stu-id="b61df-180">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="b61df-181">Valkostir birtast í fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="b61df-181">Options will appear in the drop-down list.</span></span> <span data-ttu-id="b61df-182">Smelltu eða ýttu á **Sláðu inn** til að setja inn staðgengil tilboðsgagna.</span><span class="sxs-lookup"><span data-stu-id="b61df-182">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="b61df-183">Til að tengja staðgengil við sniðmát tilboðsskjalsins án þess að sýna umsækjanda gildi þess, settu bendilinn yfir staðgengil tilboðsgagna og smelltu á **Festa** táknið.</span><span class="sxs-lookup"><span data-stu-id="b61df-183">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="b61df-184">Þetta mun ýta staðgenglinum í **Fest tilboðsgögn** hluta sniðmáts tilboðsgagnanna.</span><span class="sxs-lookup"><span data-stu-id="b61df-184">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="b61df-185">Til að taka burt skaltu fylgja sömu skrefum en smelltu **Taka burt** í listanum yfir staðgengla tilboðsgagna.</span><span class="sxs-lookup"><span data-stu-id="b61df-185">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="b61df-186">Til að skoða lista yfir virka staðgengla tilboðsgagna, skipta yfir í **Virk** flipann hægra megin í glugganum.</span><span class="sxs-lookup"><span data-stu-id="b61df-186">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="b61df-187">Ef þú setur inn staðgengil sem er keyrður af reglusetti fyrir tilboðsgögn getur þú séð tengingu þess staðgengils tilboðsgagna á öðrum gildum.</span><span class="sxs-lookup"><span data-stu-id="b61df-187">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="b61df-188">Einnig er hægt að **Flytja inn** efni úr .docx skrá á þinni vél og breyta eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b61df-188">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="b61df-189">Þannig þarftu ekki að slá inn allt innihald í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="b61df-189">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="b61df-190">Til að forskoða tilboðsskjalið er notað **Forskoðun** kost efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="b61df-190">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="b61df-191">Til að stjórna hvort stofnandi tilboðs getur breytt innihaldi tilboðsskjalsins skaltu nota **Stjórna heimild** valkostinn efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="b61df-191">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="b61df-192">Ef þú vilt að stofnandi tilboðsins setji aðeins staðgengilsgildi og ekki breytt texta skaltu stilla heimildargildið í **Nei**.</span><span class="sxs-lookup"><span data-stu-id="b61df-192">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="b61df-193">Smelltu á **Vista** til að vista framfarir þínar.</span><span class="sxs-lookup"><span data-stu-id="b61df-193">Click **Save** to save your progress.</span></span> <span data-ttu-id="b61df-194">Sniðmátið verður vistað í stöðunni drög.</span><span class="sxs-lookup"><span data-stu-id="b61df-194">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="b61df-195">Til að ljúka og merkja skjalið sem birt er skaltu smella á **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="b61df-195">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="b61df-196">Þú getur séð hvaða sniðmát skjala eru virk, í ham fyrir drög og verið geymd og eru ekki lengur í notkun í lendingarupplifun skjalasafns sniðmáta.</span><span class="sxs-lookup"><span data-stu-id="b61df-196">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="b61df-197">Þú getur eytt öllum sniðmátum tilboðsskjala sem bjóða upp á núverandi sniðmát tilboðspakka.</span><span class="sxs-lookup"><span data-stu-id="b61df-197">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="b61df-198">Sniðmát tilboðspakka</span><span class="sxs-lookup"><span data-stu-id="b61df-198">Offer package templates</span></span>

<span data-ttu-id="b61df-199">Tilboðspakkar eru tilboðsgervingar sem eru deilt með umsækjanda og samanstanda af blöndu af einu eða fleiri sniðmátum tilboðsskjala.</span><span class="sxs-lookup"><span data-stu-id="b61df-199">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="b61df-200">Til að búa til tilboðspakka skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="b61df-200">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="b61df-201">Farðu í **Stjórnun tilboða**.</span><span class="sxs-lookup"><span data-stu-id="b61df-201">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="b61df-202">Farðu í **Pakkar** frá vinstra yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b61df-202">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="b61df-203">Listi yfir virk pakkasniðmát sem eru tiltæk fyrir stofnendur tilboða til að nota birtist.</span><span class="sxs-lookup"><span data-stu-id="b61df-203">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="b61df-204">Til að búa til nýja tilboðspakka skaltu smella á **Nýr pakki**.</span><span class="sxs-lookup"><span data-stu-id="b61df-204">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="b61df-205">Sláðu inn einkvæmt heiti og smelltu **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="b61df-205">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="b61df-206">Smelltu **Bæta við sniðmáti**.</span><span class="sxs-lookup"><span data-stu-id="b61df-206">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="b61df-207">Þú getur valið að búa til nýtt sniðmát eða velja úr núverandi.</span><span class="sxs-lookup"><span data-stu-id="b61df-207">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="b61df-208">Ef þú velur að bæta við núverandi sniðmáti þarftu að ganga úr skugga um að sniðmát tilboðsskjalsins hafi verið vistað, lokað og merkt sem virkt.</span><span class="sxs-lookup"><span data-stu-id="b61df-208">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="b61df-209">Þú getur valið eins mörg sniðmát skjala eins og þú vilt.</span><span class="sxs-lookup"><span data-stu-id="b61df-209">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="b61df-210">Smelltu **Lokið** til að fara aftur í **Pakkastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="b61df-210">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="b61df-211">Þú getur stillt röð skjala og einnig merkt hvort tiltekins tilboðsskjals sé krafist við stofnun tilboðs.</span><span class="sxs-lookup"><span data-stu-id="b61df-211">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="b61df-212">Stofnandi tilboðs mun hafa möguleika á að eyða skjölum sem merktar eru sem **Ekki krafist**.</span><span class="sxs-lookup"><span data-stu-id="b61df-212">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="b61df-213">Til að vista sniðmátt tilboðspakkans svo að það sé nothæft af öllum stofnendum tilboða skaltu smella á **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="b61df-213">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="b61df-214">Til að skoða drög að sniðmátum tilboðspakka, farðu á flipann **Drög**. Ef breyting er gerð á tilboðspakka sniðmátið verður það að vera vistað og endurútgefið.</span><span class="sxs-lookup"><span data-stu-id="b61df-214">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="b61df-215">Stilltu tilboðsferli</span><span class="sxs-lookup"><span data-stu-id="b61df-215">Configure an offer process</span></span>

<span data-ttu-id="b61df-216">Það eru nokkrir hlutar stofnunarferlis tilboðs sem hægt er að stilla af stjórnanda Attract.</span><span class="sxs-lookup"><span data-stu-id="b61df-216">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="b61df-217">**Samþykki tilboða** - Veldu hvort samþykki tilboða sé krafist áður en tilboðið er hægt að senda til umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="b61df-217">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="b61df-218">Sem stjórnandi getur þú einnig ákveðið hvort öll samþykki tilboðs muni gerast í röð eða samhliða samþykki vinnuflæði.</span><span class="sxs-lookup"><span data-stu-id="b61df-218">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="b61df-219">Þú getur einnig valið hvort samþykktaraðilar tilboðs eigi að bæta við athugasemdum ásamt samþykki þeirra fyrir tilboði.</span><span class="sxs-lookup"><span data-stu-id="b61df-219">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="b61df-220">Samþykki tilboða eru nauðsynleg fyrir alla óhefðbundna tilboð.</span><span class="sxs-lookup"><span data-stu-id="b61df-220">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="b61df-221">**Tilboðsupplifun umsækjanda**- Sem stjórnandi getur þú valið að stilla hvort öll tilboð séu með lokadag, og ef svo er, hvaða sjálfgefni mótlykill fyrir lokadag ætti að vera.</span><span class="sxs-lookup"><span data-stu-id="b61df-221">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="b61df-222">Þú getur einnig stillt hvort umsækjendur geta hafnað tilboðinu.</span><span class="sxs-lookup"><span data-stu-id="b61df-222">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="b61df-223">**Rafrænar undirskriftir** - Sem stjórnandi getur þú einnig valið aðferðina sem umsækjendur geta notað til að undirrita tilboð.</span><span class="sxs-lookup"><span data-stu-id="b61df-223">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="b61df-224">Adobe Sign - Allir tilboðspakkar verða sendir og undirritaðir með Adobe Sign.</span><span class="sxs-lookup"><span data-stu-id="b61df-224">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="b61df-225">Stofnendur tilboða sem gefur út tilboðið verða að hafa Adobe Sign reikninginn sinn tengdan við Attract.</span><span class="sxs-lookup"><span data-stu-id="b61df-225">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="b61df-226">Fyrir Adobe Sign-leyfi og ókeypis prufuútgáfu skal heimsækja [tengill](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="b61df-226">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="b61df-227">DocuSign - Allir tilboðspakkar verða sendir og undirritaðir með DocuSign.</span><span class="sxs-lookup"><span data-stu-id="b61df-227">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="b61df-228">Stofnendur tilboða sem gefur út tilboðið verða að hafa DocuSign reikninginn sinn tengdan við Attract.</span><span class="sxs-lookup"><span data-stu-id="b61df-228">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="b61df-229">ESign - Þetta er sjálfgefinn valkostur, sem fylgir beint úr kassanum, þar sem notandinn getur skrifað undir tilboð með því að slá inn nafn og upphafsstafi.</span><span class="sxs-lookup"><span data-stu-id="b61df-229">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="b61df-230">Til að læra meira um stofnunarferli tilboðs, sjá [Stofna, samþykkja og undirrita tilboð](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="b61df-230">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>
