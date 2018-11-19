---
title: "Snjallmeðmæli"
description: "Þetta efnisatriði útskýrir hvernig hægt er að nota vélnám til að veita ráðleggingar fyrir störf og umsækjendur."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.contentlocale: is-is
ms.lasthandoff: 11/12/2018

---

# <a name="intelligent-recommendations"></a><span data-ttu-id="8d334-103">Snjallmeðmæli</span><span class="sxs-lookup"><span data-stu-id="8d334-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8d334-104">Vélnám getur hjálpað ráðningaraðilum og mannauðsstjórum til að auðkenna skjótt bestu umsækjendurna fyrir starf.</span><span class="sxs-lookup"><span data-stu-id="8d334-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="8d334-105">Það getur einnig hjálpað umsækjendum að finna starfið sem best hentar forstillingum þeirra og áhugamálum.</span><span class="sxs-lookup"><span data-stu-id="8d334-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="8d334-106">Um leið og þessar aðgerðir eru notaðar og endurgjöf er veitt munu tillögur batna.</span><span class="sxs-lookup"><span data-stu-id="8d334-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="8d334-107">Eiginleikar snjallmeðmæla eru aðeins í boði með Viðbót við alhliða ráðningar.</span><span class="sxs-lookup"><span data-stu-id="8d334-107">The intelligent recommendation features are available only with the Comprehensive hiring add-on.</span></span>
> - <span data-ttu-id="8d334-108">Til að virkja umsækjandann og eiginleika starfstilboðsins þarf stjórnandi að kveikja á forskoðunarvalkostum fyrir þau.</span><span class="sxs-lookup"><span data-stu-id="8d334-108">To enable the candidate and job recommendation features, an admin must turn on the preview options for them.</span></span> <span data-ttu-id="8d334-109">Í stjórnandamiðstöðinni, á **Eiginleikastjórnun** flipanum skaltu ganga úr skugga um að **Forskoðunareiginleikar** valkostur er stillt á **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="8d334-109">In the Admin center, on the **Feature management** tab, make sure that the **Preview features** option is set to **On**.</span></span> <span data-ttu-id="8d334-110">Gakktu úr skugga um að einstakir valkostir fyrir **Umsækjandi sem mælt er með** og **Starfsmeðmæli** séu stilltir á **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="8d334-110">Then make sure that the individual **Candidate recommendation** and **Job recommendation** options are set to **On**.</span></span>

## <a name="candidate-recommendations"></a><span data-ttu-id="8d334-111">Umsækjendur sem mælt er með</span><span class="sxs-lookup"><span data-stu-id="8d334-111">Candidate recommendations</span></span>

<span data-ttu-id="8d334-112">Vegna þess að starfsauglýsingar gæti laðað hundruð umsækjenda getur það verið erfitt fyrir ráðningaraðila og mannauðsstjóra að finna umsækjendur sem eru hæfir og með bakgrunn sem hentar starfinu.</span><span class="sxs-lookup"><span data-stu-id="8d334-112">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="8d334-113">Með því að greina samsvörun milli starfslýsingarinnar og hæfniskrafa, og gögn frá ferilsskrám frambjóðendum og forstillingum, er hægt að nota vélnám til að kalla fram meðmæli umsækjenda.</span><span class="sxs-lookup"><span data-stu-id="8d334-113">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="8d334-114">Meðmæli umsækjenda geta hjálpað ráðningaraðila og mannauðsstjóra að bera kennsl á hæfileikaríkustu einstaklingana og flytja þá hraðar yfir í viðtalsferlið.</span><span class="sxs-lookup"><span data-stu-id="8d334-114">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="8d334-115">Fyrir hvaða starf sem er, ef fleiri en tíu umsækjendur eða viðföng eru með ferilsskrár eða heilstæðar forstillingar, birtast umsækjendur eða viðföng sem nánast uppfylla starfskröfur í **Umsækjendur til að hafa í huga** hlutanum á **Starf** síðunni.</span><span class="sxs-lookup"><span data-stu-id="8d334-115">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="8d334-116">Fyrir hvern umsækjanda sem er mælt með er hægt að velja **Skoða umsækjanda** á spjaldi umsækjandans til að skoða forstillingar umsækjanda og grípa til aðgerða varðandi umsókn hans eða hennar.</span><span class="sxs-lookup"><span data-stu-id="8d334-116">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="8d334-117">Þú getur notað þrípunktahnappinn (**...**) til að opna forstillingar umsækjanda á nýjum flipa. Þú getur einnig notað þrípunktanappinn til að veita endurgjöf um meðmæli.</span><span class="sxs-lookup"><span data-stu-id="8d334-117">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="8d334-118">Þannig færðu aðstoð við að fínstilla uppástungur forritsins og bæta ábendingar í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="8d334-118">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="8d334-119">Öll meðmæli sem þér líkar ekki við eru fjarlægðar úr **Umsækjendur til að hafa í huga** hlutanum þegar þú endurhleður **Starf** síðuna.</span><span class="sxs-lookup"><span data-stu-id="8d334-119">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="8d334-120">Þú getur notað spjaldið fyrir endurgjöf til að gefa kynna af hverju þú fannst ekki meðmælin gagnleg.</span><span class="sxs-lookup"><span data-stu-id="8d334-120">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="8d334-121">Tillögur um störf</span><span class="sxs-lookup"><span data-stu-id="8d334-121">Job recommendations</span></span> 

<span data-ttu-id="8d334-122">Þegar væntanlegur starfsmaður notar starfatorgið til að sækja um starf er mælt með öðrum lausum störfum hjá fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="8d334-122">When a prospective employee uses the career site to apply to a job, other open positions at the organization are recommended.</span></span> <span data-ttu-id="8d334-123">Þessar tillögur eru byggðar á fyrri umsóknum viðfangsins og ferilskrá umsækjandans eða forstillingum hans eða hennar.</span><span class="sxs-lookup"><span data-stu-id="8d334-123">These recommendations are based on the prospect's past applications, and on his or her resume or candidate profile.</span></span> <span data-ttu-id="8d334-124">Þar af leiðandi eru tillögur um störf sem hjálpa viðföngum að greina fljótt þau störf sem eru best fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="8d334-124">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="8d334-125">Tillögur um störf eru veittar til viðfanga ef fleiri en tíu störf eru auglýst á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="8d334-125">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="8d334-126">Viðföng geta opnað upplýsingar um starfsauglýsingar á spjaldinu fyrir meðmæli.</span><span class="sxs-lookup"><span data-stu-id="8d334-126">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="8d334-127">Þeir geta einnig veitt endurgöf um tillögur til að bæta ábendingar í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="8d334-127">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>

