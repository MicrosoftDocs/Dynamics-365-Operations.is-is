## <a name="cds-contacts-v2-to-contacts"></a><span data-ttu-id="9e668-101">Tengiliðir fyrir skuldatryggingu V2 til tengiliða</span><span class="sxs-lookup"><span data-stu-id="9e668-101">CDS Contacts V2 to contacts</span></span>

<span data-ttu-id="9e668-102">Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9e668-102">This template synchronizes data between Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="9e668-103">Upprunasía: (AssociatedContactType = 1)</span><span class="sxs-lookup"><span data-stu-id="9e668-103">Source filter: (AssociatedContactType = 1)</span></span>

<span data-ttu-id="9e668-104">Bakfærð upprunasía: msdyn_contactforvendor eq true og msdyn_sellable eq false og msdyn_contactpersonid ne ''</span><span class="sxs-lookup"><span data-stu-id="9e668-104">Reversed source filter: msdyn_contactforvendor eq true and msdyn_sellable eq false and msdyn_contactpersonid ne ''</span></span>

<span data-ttu-id="9e668-105">Svæði í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9e668-105">Finance and Operations field</span></span> | <span data-ttu-id="9e668-106">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="9e668-106">Map type</span></span> | <span data-ttu-id="9e668-107">Annar Dynamics 365 reitur</span><span class="sxs-lookup"><span data-stu-id="9e668-107">Other Dynamics 365 field</span></span> | <span data-ttu-id="9e668-108">Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="9e668-108">Default value</span></span>
---|---|---|---
<span data-ttu-id="9e668-109">CONTACTPERSONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="9e668-109">CONTACTPERSONPARTYNUMBER</span></span> | = | <span data-ttu-id="9e668-110">msdyn_partynumber</span><span class="sxs-lookup"><span data-stu-id="9e668-110">msdyn_partynumber</span></span> | 
<span data-ttu-id="9e668-111">ASSOCIATEDCONTACTTYPE</span><span class="sxs-lookup"><span data-stu-id="9e668-111">ASSOCIATEDCONTACTTYPE</span></span> | << | <span data-ttu-id="9e668-112">ekkert</span><span class="sxs-lookup"><span data-stu-id="9e668-112">none</span></span> | <span data-ttu-id="9e668-113">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="9e668-113">Vendor</span></span>
<span data-ttu-id="9e668-114">FIRSTNAME</span><span class="sxs-lookup"><span data-stu-id="9e668-114">FIRSTNAME</span></span> | = | <span data-ttu-id="9e668-115">firstname</span><span class="sxs-lookup"><span data-stu-id="9e668-115">firstname</span></span> | 
<span data-ttu-id="9e668-116">MIDDLENAME</span><span class="sxs-lookup"><span data-stu-id="9e668-116">MIDDLENAME</span></span> | = | <span data-ttu-id="9e668-117">middlename</span><span class="sxs-lookup"><span data-stu-id="9e668-117">middlename</span></span> | 
<span data-ttu-id="9e668-118">EFTIRNAFN</span><span class="sxs-lookup"><span data-stu-id="9e668-118">LASTNAME</span></span> | = | <span data-ttu-id="9e668-119">lastname</span><span class="sxs-lookup"><span data-stu-id="9e668-119">lastname</span></span> | 
<span data-ttu-id="9e668-120">ASSOCIATEDCONTACTNUMBER</span><span class="sxs-lookup"><span data-stu-id="9e668-120">ASSOCIATEDCONTACTNUMBER</span></span> | = | <span data-ttu-id="9e668-121">msdyn_vendorcontactid.msdyn_vendoraccountnumber</span><span class="sxs-lookup"><span data-stu-id="9e668-121">msdyn_vendorcontactid.msdyn_vendoraccountnumber</span></span> | 
<span data-ttu-id="9e668-122">PRIMARYADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="9e668-122">PRIMARYADDRESSCITY</span></span> | = | <span data-ttu-id="9e668-123">address1_city</span><span class="sxs-lookup"><span data-stu-id="9e668-123">address1_city</span></span> | 
<span data-ttu-id="9e668-124">PRIMARYADDRESSCOUNTRYREGIONID</span><span class="sxs-lookup"><span data-stu-id="9e668-124">PRIMARYADDRESSCOUNTRYREGIONID</span></span> | = | <span data-ttu-id="9e668-125">address1_country</span><span class="sxs-lookup"><span data-stu-id="9e668-125">address1_country</span></span> | 
<span data-ttu-id="9e668-126">PRIMARYADDRESSCOUNTYID</span><span class="sxs-lookup"><span data-stu-id="9e668-126">PRIMARYADDRESSCOUNTYID</span></span> | = | <span data-ttu-id="9e668-127">address1_county</span><span class="sxs-lookup"><span data-stu-id="9e668-127">address1_county</span></span> | 
<span data-ttu-id="9e668-128">PRIMARYFAXNUMBER</span><span class="sxs-lookup"><span data-stu-id="9e668-128">PRIMARYFAXNUMBER</span></span> | = | <span data-ttu-id="9e668-129">fax</span><span class="sxs-lookup"><span data-stu-id="9e668-129">fax</span></span> | 
<span data-ttu-id="9e668-130">PRIMARYADDRESSSTATEID</span><span class="sxs-lookup"><span data-stu-id="9e668-130">PRIMARYADDRESSSTATEID</span></span> | = | <span data-ttu-id="9e668-131">address1_stateorprovince</span><span class="sxs-lookup"><span data-stu-id="9e668-131">address1_stateorprovince</span></span> | 
<span data-ttu-id="9e668-132">PRIMARYADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="9e668-132">PRIMARYADDRESSSTREET</span></span> | = | <span data-ttu-id="9e668-133">address1_line1</span><span class="sxs-lookup"><span data-stu-id="9e668-133">address1_line1</span></span> | 
<span data-ttu-id="9e668-134">PRIMARYADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="9e668-134">PRIMARYADDRESSZIPCODE</span></span> | = | <span data-ttu-id="9e668-135">address1_postalcode</span><span class="sxs-lookup"><span data-stu-id="9e668-135">address1_postalcode</span></span> | 
<span data-ttu-id="9e668-136">PRIMARYPHONENUMBER</span><span class="sxs-lookup"><span data-stu-id="9e668-136">PRIMARYPHONENUMBER</span></span> | = | <span data-ttu-id="9e668-137">telephone1</span><span class="sxs-lookup"><span data-stu-id="9e668-137">telephone1</span></span> | 
<span data-ttu-id="9e668-138">PRIMARYEMAILADDRESS</span><span class="sxs-lookup"><span data-stu-id="9e668-138">PRIMARYEMAILADDRESS</span></span> | = | <span data-ttu-id="9e668-139">emailaddress1</span><span class="sxs-lookup"><span data-stu-id="9e668-139">emailaddress1</span></span> | 
<span data-ttu-id="9e668-140">EMPLOYMENTDEPARTMENT</span><span class="sxs-lookup"><span data-stu-id="9e668-140">EMPLOYMENTDEPARTMENT</span></span> | = | <span data-ttu-id="9e668-141">deild</span><span class="sxs-lookup"><span data-stu-id="9e668-141">department</span></span> | 
<span data-ttu-id="9e668-142">ATHUGASEMDIR</span><span class="sxs-lookup"><span data-stu-id="9e668-142">NOTES</span></span> | = | <span data-ttu-id="9e668-143">lýsing</span><span class="sxs-lookup"><span data-stu-id="9e668-143">description</span></span> | 
<span data-ttu-id="9e668-144">GENDER</span><span class="sxs-lookup"><span data-stu-id="9e668-144">GENDER</span></span> | >< | <span data-ttu-id="9e668-145">gendercode</span><span class="sxs-lookup"><span data-stu-id="9e668-145">gendercode</span></span> | 
<span data-ttu-id="9e668-146">GOVERNMENTIDENTIFICATIONNUMBER</span><span class="sxs-lookup"><span data-stu-id="9e668-146">GOVERNMENTIDENTIFICATIONNUMBER</span></span> | = | <span data-ttu-id="9e668-147">governmentid</span><span class="sxs-lookup"><span data-stu-id="9e668-147">governmentid</span></span> | 
<span data-ttu-id="9e668-148">PRIMARYURL</span><span class="sxs-lookup"><span data-stu-id="9e668-148">PRIMARYURL</span></span> | = | <span data-ttu-id="9e668-149">websiteurl</span><span class="sxs-lookup"><span data-stu-id="9e668-149">websiteurl</span></span> | 
<span data-ttu-id="9e668-150">MARITALSTATUS</span><span class="sxs-lookup"><span data-stu-id="9e668-150">MARITALSTATUS</span></span> | >< | <span data-ttu-id="9e668-151">familystatuscode</span><span class="sxs-lookup"><span data-stu-id="9e668-151">familystatuscode</span></span> | 
<span data-ttu-id="9e668-152">ISRECEIVINGDIRECTMAIL</span><span class="sxs-lookup"><span data-stu-id="9e668-152">ISRECEIVINGDIRECTMAIL</span></span> | >< | <span data-ttu-id="9e668-153">donotemail</span><span class="sxs-lookup"><span data-stu-id="9e668-153">donotemail</span></span> | 
<span data-ttu-id="9e668-154">EMPLOYMENTPROFESSION</span><span class="sxs-lookup"><span data-stu-id="9e668-154">EMPLOYMENTPROFESSION</span></span> | = | <span data-ttu-id="9e668-155">jobtitle</span><span class="sxs-lookup"><span data-stu-id="9e668-155">jobtitle</span></span> | 
<span data-ttu-id="9e668-156">SPOUSENAME</span><span class="sxs-lookup"><span data-stu-id="9e668-156">SPOUSENAME</span></span> | = | <span data-ttu-id="9e668-157">nafn maka</span><span class="sxs-lookup"><span data-stu-id="9e668-157">spousesname</span></span> | 
<span data-ttu-id="9e668-158">ekkert</span><span class="sxs-lookup"><span data-stu-id="9e668-158">none</span></span> | >> | <span data-ttu-id="9e668-159">msdyn_contactforvendor</span><span class="sxs-lookup"><span data-stu-id="9e668-159">msdyn_contactforvendor</span></span> | <span data-ttu-id="9e668-160">Satt</span><span class="sxs-lookup"><span data-stu-id="9e668-160">True</span></span>
<span data-ttu-id="9e668-161">CONTACTPERSONID</span><span class="sxs-lookup"><span data-stu-id="9e668-161">CONTACTPERSONID</span></span> | = | <span data-ttu-id="9e668-162">msdyn_contactpersonid</span><span class="sxs-lookup"><span data-stu-id="9e668-162">msdyn_contactpersonid</span></span> | 