## <a name="main-account-to-msdyn_mainaccounts"></a><span data-ttu-id="a3cbb-101">Aðallykill í msdyn_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="a3cbb-101">Main account to msdyn_mainaccounts</span></span>

<span data-ttu-id="a3cbb-102">Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a3cbb-102">This template synchronizes data between Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="a3cbb-103">Svæði í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a3cbb-103">Finance and Operations field</span></span> | <span data-ttu-id="a3cbb-104">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="a3cbb-104">Map type</span></span> | <span data-ttu-id="a3cbb-105">Annar Dynamics 365 reitur</span><span class="sxs-lookup"><span data-stu-id="a3cbb-105">Other Dynamics 365 field</span></span> | <span data-ttu-id="a3cbb-106">Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="a3cbb-106">Default value</span></span>
---|---|---|---
<span data-ttu-id="a3cbb-107">MAINACCOUNTID</span><span class="sxs-lookup"><span data-stu-id="a3cbb-107">MAINACCOUNTID</span></span> | = | <span data-ttu-id="a3cbb-108">msdyn_accountnumber</span><span class="sxs-lookup"><span data-stu-id="a3cbb-108">msdyn_accountnumber</span></span> | 
<span data-ttu-id="a3cbb-109">CHARTOFACCOUNTS</span><span class="sxs-lookup"><span data-stu-id="a3cbb-109">CHARTOFACCOUNTS</span></span> | = | <span data-ttu-id="a3cbb-110">msdyn_chartofaccounts.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="a3cbb-110">msdyn_chartofaccounts.msdyn_name</span></span> | 
<span data-ttu-id="a3cbb-111">HEITI</span><span class="sxs-lookup"><span data-stu-id="a3cbb-111">NAME</span></span> | = | <span data-ttu-id="a3cbb-112">msdyn_name</span><span class="sxs-lookup"><span data-stu-id="a3cbb-112">msdyn_name</span></span> | 
<span data-ttu-id="a3cbb-113">BALANCECONTROL</span><span class="sxs-lookup"><span data-stu-id="a3cbb-113">BALANCECONTROL</span></span> | >< | <span data-ttu-id="a3cbb-114">msdyn_balancecontrol</span><span class="sxs-lookup"><span data-stu-id="a3cbb-114">msdyn_balancecontrol</span></span> | 
<span data-ttu-id="a3cbb-115">EXCHANGEADJUSTMENTRATETYPE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-115">EXCHANGEADJUSTMENTRATETYPE</span></span> | = | <span data-ttu-id="a3cbb-116">msdyn_exchangeadjustmentratetype.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="a3cbb-116">msdyn_exchangeadjustmentratetype.msdyn_name</span></span> | 
<span data-ttu-id="a3cbb-117">CLOSING</span><span class="sxs-lookup"><span data-stu-id="a3cbb-117">CLOSING</span></span> | >< | <span data-ttu-id="a3cbb-118">msdyn_closing</span><span class="sxs-lookup"><span data-stu-id="a3cbb-118">msdyn_closing</span></span> | 
<span data-ttu-id="a3cbb-119">REPORTINGEXCHANGEADJUSTMENTRATETYPE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-119">REPORTINGEXCHANGEADJUSTMENTRATETYPE</span></span> | = | <span data-ttu-id="a3cbb-120">msdyn_reportingexchangeadjustmentratetype.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="a3cbb-120">msdyn_reportingexchangeadjustmentratetype.msdyn_name</span></span> | 
<span data-ttu-id="a3cbb-121">DEBITCREDITREQUIREMENT</span><span class="sxs-lookup"><span data-stu-id="a3cbb-121">DEBITCREDITREQUIREMENT</span></span> | >< | <span data-ttu-id="a3cbb-122">msdyn_debitcreditrequirement</span><span class="sxs-lookup"><span data-stu-id="a3cbb-122">msdyn_debitcreditrequirement</span></span> | 
<span data-ttu-id="a3cbb-123">FINANCIALREPORTINGEXCHANGERATETYPE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-123">FINANCIALREPORTINGEXCHANGERATETYPE</span></span> | = | <span data-ttu-id="a3cbb-124">msdyn_financialreportingexchangeratetype.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="a3cbb-124">msdyn_financialreportingexchangeratetype.msdyn_name</span></span> | 
<span data-ttu-id="a3cbb-125">FOREIGNCURRENCYREVALUATION</span><span class="sxs-lookup"><span data-stu-id="a3cbb-125">FOREIGNCURRENCYREVALUATION</span></span> | >< | <span data-ttu-id="a3cbb-126">msdyn_foreigncurrencyrevaluation</span><span class="sxs-lookup"><span data-stu-id="a3cbb-126">msdyn_foreigncurrencyrevaluation</span></span> | 
<span data-ttu-id="a3cbb-127">MAINACCOUNTCATEGORY</span><span class="sxs-lookup"><span data-stu-id="a3cbb-127">MAINACCOUNTCATEGORY</span></span> | = | <span data-ttu-id="a3cbb-128">msdyn_mainaccountcategoryname</span><span class="sxs-lookup"><span data-stu-id="a3cbb-128">msdyn_mainaccountcategoryname</span></span> | 
<span data-ttu-id="a3cbb-129">MANDATORYPAYMENTREFERENCE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-129">MANDATORYPAYMENTREFERENCE</span></span> | >< | <span data-ttu-id="a3cbb-130">msdyn_mandatorypaymentreference</span><span class="sxs-lookup"><span data-stu-id="a3cbb-130">msdyn_mandatorypaymentreference</span></span> | 
<span data-ttu-id="a3cbb-131">MONETARY</span><span class="sxs-lookup"><span data-stu-id="a3cbb-131">MONETARY</span></span> | >< | <span data-ttu-id="a3cbb-132">msdyn_monetary</span><span class="sxs-lookup"><span data-stu-id="a3cbb-132">msdyn_monetary</span></span> | 
<span data-ttu-id="a3cbb-133">OFFSETACCOUNTDISPLAYVALUE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-133">OFFSETACCOUNTDISPLAYVALUE</span></span> | = | <span data-ttu-id="a3cbb-134">msdyn_offsetaccount</span><span class="sxs-lookup"><span data-stu-id="a3cbb-134">msdyn_offsetaccount</span></span> | 
<span data-ttu-id="a3cbb-135">POSTINGTYPE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-135">POSTINGTYPE</span></span> | >< | <span data-ttu-id="a3cbb-136">msdyn_postingtype</span><span class="sxs-lookup"><span data-stu-id="a3cbb-136">msdyn_postingtype</span></span> | 
<span data-ttu-id="a3cbb-137">SRUCODE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-137">SRUCODE</span></span> | = | <span data-ttu-id="a3cbb-138">msdyn_srucode</span><span class="sxs-lookup"><span data-stu-id="a3cbb-138">msdyn_srucode</span></span> | 
<span data-ttu-id="a3cbb-139">VALIDATECURRENCY</span><span class="sxs-lookup"><span data-stu-id="a3cbb-139">VALIDATECURRENCY</span></span> | >< | <span data-ttu-id="a3cbb-140">msdyn_validatecurrencycode</span><span class="sxs-lookup"><span data-stu-id="a3cbb-140">msdyn_validatecurrencycode</span></span> | 
<span data-ttu-id="a3cbb-141">VALIDATEUSER</span><span class="sxs-lookup"><span data-stu-id="a3cbb-141">VALIDATEUSER</span></span> | >< | <span data-ttu-id="a3cbb-142">msdyn_validateuser</span><span class="sxs-lookup"><span data-stu-id="a3cbb-142">msdyn_validateuser</span></span> | 
<span data-ttu-id="a3cbb-143">DEBITCREDITDEFAULT</span><span class="sxs-lookup"><span data-stu-id="a3cbb-143">DEBITCREDITDEFAULT</span></span> | >< | <span data-ttu-id="a3cbb-144">msdyn_debitcreditdefault</span><span class="sxs-lookup"><span data-stu-id="a3cbb-144">msdyn_debitcreditdefault</span></span> | 
<span data-ttu-id="a3cbb-145">DEFAULTCURRENCY</span><span class="sxs-lookup"><span data-stu-id="a3cbb-145">DEFAULTCURRENCY</span></span> | = | <span data-ttu-id="a3cbb-146">msdyn_defaultcurrency.isocurrencycode</span><span class="sxs-lookup"><span data-stu-id="a3cbb-146">msdyn_defaultcurrency.isocurrencycode</span></span> | 
<span data-ttu-id="a3cbb-147">MAINACCOUNTTYPE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-147">MAINACCOUNTTYPE</span></span> | >< | <span data-ttu-id="a3cbb-148">msdyn_mainaccounttype</span><span class="sxs-lookup"><span data-stu-id="a3cbb-148">msdyn_mainaccounttype</span></span> | 
<span data-ttu-id="a3cbb-149">FINANCIALREPORTINGCURRENCYTRANSLATIONTYPE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-149">FINANCIALREPORTINGCURRENCYTRANSLATIONTYPE</span></span> | >< | <span data-ttu-id="a3cbb-150">msdyn_financialreportingcurrencytrantype</span><span class="sxs-lookup"><span data-stu-id="a3cbb-150">msdyn_financialreportingcurrencytrantype</span></span> | 
<span data-ttu-id="a3cbb-151">USER</span><span class="sxs-lookup"><span data-stu-id="a3cbb-151">USER</span></span> | = | <span data-ttu-id="a3cbb-152">msdyn_user</span><span class="sxs-lookup"><span data-stu-id="a3cbb-152">msdyn_user</span></span> | 
<span data-ttu-id="a3cbb-153">VALIDATEPOSTINGTYPE</span><span class="sxs-lookup"><span data-stu-id="a3cbb-153">VALIDATEPOSTINGTYPE</span></span> | >< | <span data-ttu-id="a3cbb-154">msdyn_validateposting</span><span class="sxs-lookup"><span data-stu-id="a3cbb-154">msdyn_validateposting</span></span> | 