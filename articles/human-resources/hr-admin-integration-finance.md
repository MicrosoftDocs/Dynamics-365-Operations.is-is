---
title: Skilgreina samþættingu við Finance
description: Þessi grein lýsir samþættingu á milli Dynamics 365 Human Resources og Dynamics 365 Finance.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8be7cbf92c11036d334516116f0895c426380954
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875859"
---
# <a name="configure-integration-with-finance"></a>Skilgreina samþættingu við Finance


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Að samþætta Dynamics 365 Human Resources með Dynamics 365 Finance geturðu notað sniðmátið Mannauður til að fjármagna í [Gagnasamþættari](/powerapps/administrator/data-integrator). Sniðmát Human Resources til Finance gerir gagnaflæði kleift fyrir störf, stöður og starfsmenn. Sniðmátið leyfir gögnum að flæða úr Human Resources yfir í Finance, en leyfa ekki gögnum að streyma frá Finance til Human Resources.

![Samþættingarferli Human Resources til Finance.](./media/hr-admin-integration-finance-flow.png)

Lausn Human Resources til Finance veitir eftirfarandi tegundir samstillingar gagna:

- Viðhalda vinnslum í Human Resources og samstilla þær úr Human Resources til Finance.
- Viðhalda stöðum og stöðuúthlutunum í Human Resources og samstilla þau úr Human Resources til Finance
- Viðhalda störfum í Human Resources og samstilla þau úr Human Resources til Finance
- Viðhalda starfskröftum og heimilisföngum starfskrafta í Human Resources og samstilla þá úr Human Resources til Finance

## <a name="system-requirements-for-human-resources"></a>Kerfiskröfur vegna Human Resources

Sameiningalausnin krefst eftirfarandi útgáfa af Human Resources og Finance: 

- Dynamics 365 Human Resources á Dataverse
- Dynamics 365 Finance útgáfa 7.2 og nýrri

## <a name="template-and-tasks"></a>Sniðmát og verkefni

Til að fá aðgang að sniðmáti Human Resources og Finance.

1. Opnaðu [Power Apps stjórnendamiðstöðina](https://admin.powerapps.com/). 

2. Veldu **Verk** og veldu síðan **Nýtt verk** í efra hægra horninu. Stofnaðu nýtt verk fyrir hvern lögaðila sem þú vilt samþætta inn í Finance.

3. Veldu **Human Resources (Human Resources Dataverse í Finance)** til að samstilla skrár úr Human Resources í Finance.

Sniðmátið notar eftirfarandi undirliggandi verk til að samstilla skrár úr Human Resources við Finance:

- **Starfshlutverk til bóta starfshlutverk**
- **Deildir til rekstrareiningar**
- **Tegund gerða til bóta**
- **Störf til starfa**
- **Störf til starfsupplýsinga**
- **Stöðugerðir að stöðugerð**
- **Starfsstöður til grunnstöðu**
- **Upplýsingar frá starfi til starfs**
- **Tímalengd frá starfi til starfs**
- **Stigveldi frá starfi til starfs**
- **Starfskraftar til starfskrafts**
- **Atvinna til atvinnu**
- **Upplýsingar atvinnu til atvinnu**
- **Stöðuúthlutun starfskrafts á stöðuúthlutanir starfskrafta**
- **Heimilisföng starfsmanns til póstfangs starfsmanns V2**

## <a name="template-mappings"></a>Varpanir sniðmáta

Í eftirfarandi kortum yfir kortlagningartöflu inniheldur nafn verksins þær einingar sem notaðar eru í hverju forriti. Gjafinn (Human Resources) er til vinstri og áfangastaðurinn (Finance) er til hægri.

### <a name="job-functions-to-compensation-job-function"></a>Starfshlutverk til bóta starfshlutverk

| Dataverse tafla (uppruni) | Finance eining (áfangastaður) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Heiti falls)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>Deildir til rekstrareiningar

| Dataverse tafla (uppruni)           | Finance eining (áfangastaður) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Tegund gerða til bóta

| Dataverse tafla (uppruni)   | Finance eining (áfangastaður) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Störf til starfa

| Dataverse tafla (uppruni)                           | Finance eining (áfangastaður)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Störf til starfsupplýsinga

| Dataverse tafla (uppruni)                             | Finance eining (áfangastaður) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (starfstegund (starfstegundarheiti))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Starfshlutverk (Nafn starfsaðgerða)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (gilt frá)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (gildir til)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Sjálfgefið stöðugildi)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Stöðugerðir að stöðugerð

| Dataverse tafla (uppruni)       | Finance eining (áfangastaður) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>Starfsstöður til grunnstöðu

| Dataverse tafla (uppruni)           | Finance eining (áfangastaður) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (starfstölunúmer) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Upplýsingar frá starfi til starfs

| Dataverse tafla (uppruni)              | Finance eining (áfangastaður)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (starfstöðunúmer)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (starf (heiti))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (deild (deildarnúmer)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (stöðutegund (nafn))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (í boði fyrir úthlutun)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (gilt frá)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (gildir til)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (fullt stöðugildi)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Tímalengd frá starfi til starfs

| Dataverse tafla (uppruni)             | Finance eining (áfangastaður) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (starfstölunúmer)   | POSITIONID (POSITIONID)                      |
| Calculated   Activation (reiknuð virkjun) | VALIDFROM (VALIDFROM)                        |
| Calculated   Retirement (reiknuð eftirlaun) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>Stigveldi frá starfi til starfs

| Dataverse tafla (uppruni)        | Finance eining (áfangastaður) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (starfstölunúmer)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (gilt frá)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (gildir   til)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Starfskraftar til starfskrafts
| Dataverse tafla (uppruni)           | Finance eining (áfangastaður)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Atvinna til atvinnu

| Dataverse tafla (uppruni)                             | Finance eining (áfangastaður) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Upplýsingar atvinnu til atvinnu

| Dataverse tafla (uppruni)                             | Finance eining (áfangastaður)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (gilt frá)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (gildir   til)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Stöðuúthlutun starfskrafts á stöðuúthlutanir starfskrafta

| Dataverse tafla (uppruni)                             | Finance eining (áfangastaður)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (starfstölunúmer)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (gilt frá)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (gildir til)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Heimilisföng starfsmanns til póstfangs starfsmanns V2

| Dataverse tafla (uppruni)                             | Finance eining (áfangastaður)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Hvað skal hafa í huga við samþættingu

Samþætting úr Human Resources til Finance reynir að samsvara gögnum sem byggjast á auðkenni. Ef skrárnar stemma yfirskrifar gagnasamþættingin gögnin í Finance með gildunum í Human Resources. Hins vegar getur komið upp vandamál ef rökrétt er að þetta eru mismunandi skrár og sama auðkenni var búið til í annaðhvort Human Resources eða Finance miðað við viðkomandi númeraröð.

Þetta vandamál getur orðið með **starfskrafti**, sem notar **starfsmannanúmer** til að gera samsvörun og **stöður**. Störf nota ekki númeraraðir. Þar af leiðandi, ef sama verkauðkenni er til í bæði mannauði og fjármálum, skrifa mannauðsupplýsingarnar yfir Dynamics 365 Finance upplýsingarnar. 

Til að koma í veg fyrir vandamál með afritunarauðkenni geturðu annaðhvort bætt við forskeyti á [númeraröð](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json), eða stilltu upphafsnúmer á númeraröðina sem er umfram svið hins kerfisins. 

Staðarauðkenni sem notað er fyrir heimilisfang starfsmanns er ekki hluti af númeraröð. Þegar samþætt er heimilisfang starfsmanns úr Human Resources til Finance, ef heimilisfang starfsmanns er þegar til í Finance, getur verið búið til afrit heimilisfang. 

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþáttara. 

![Vörpun sniðmáts.](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
