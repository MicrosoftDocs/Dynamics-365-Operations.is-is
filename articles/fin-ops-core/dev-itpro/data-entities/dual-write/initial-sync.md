---
title: Ósjálfstæð keðja einingar (samstillingarröð)
description: Þetta efni tilgreinir röð samstillingarinnar sem þú verður að fylgja til að búa til upphafsgögnin.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275488"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Ósjálfstæð keðja einingar (samstillingarröð)

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði tilgreinir röð samstillingarinnar sem þú verður að fylgja til að búa til upphafsgögnin ef þú ert ekki að nota einingatengsl frá eiginleikanum **fyrsta samstilling**. Ef þú ert ekki að nota **fyrstu samstillingu**, verður þú að keyra hvert einingakort fyrir sig.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management einingar

Eftirfarandi einingar fyrir Supply Chain Management eru skráðar í þeirri röð sem ætti að virkja þær.

| Heiti vörpunar á síðunni Tvíritun | Heiti lýsigagna einingar í Supply Chain Management | Heiti lýsigagna einingar í Common Data Service | Athugasemdir |
|---|---|---|---|
| Einingar ... uoms                                                                      | UnitOfMeasureEntity                                    | mælieining                                          | |
| Umreikningur eininga ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Allar afurðir ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Afurðavíddaflokkar ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Geymsluvíddarflokkar ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Rakningarvíddarflokkur ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Litir ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Stærðir ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Stílar ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Grunnstillingar ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Útgefnar afurðir V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service útgefnar einkvæmar afurðir ... afurðir                         | EcoResReleasedDistinctProductCommon Data ServiceEining | vara                                      | |
| Afurðarnúmer sem eru auðkennd með strikamerki ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Sjálfgefnar pöntunarstillingar ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Sjálfgefnar afurðapöntunarstillingar V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Sjálfgefnar afurðapöntunarstillingar ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Svæði ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Vöruhús ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Sjá [athugasemd 1](#scm-notes). |
| Litir afurðarsniðmáts ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Stærðir afurðarsniðmáts ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Stílar afurðarsniðmáts ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Grunnstillingar afurðarsniðmáts ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Afurðaflokkar ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Sjá [athugasemd 2](#scm-notes). |
| Úthlutanir afurðategundar ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Afurðaflokkastigveldi ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Afurðarnúmer sem eru auðkennd með strikamerki ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Birgðagangur ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Vöruhúsasvæði ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Svæðishópar vöruhúss ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Vöruhúsastaðsetningar ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Sjá [athugasemd 3](#scm-notes). |
| Vinnuhausar vöruhúss ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Vinnulínur vöruhúsa ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Sjá [athugasemd 4](#scm-notes). |
| Afhendingarmátar ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Afhendingarskilmálar ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Upprunakóðar sölupöntunar ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service sölupöntunarhausar ... salesorders                             | SalesOrderHeaderCommon Data ServiceEining              | salesorder                                   | |
| Common Data Service sölupöntunarlínur ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEining                | salesorderdetails                            | |
| Common Data Service sölutilboðshaus ... quotes                               | SalesQuotationHeaderCommon Data ServiceEining          | tilboð                                        | |
| Common Data Service sölutilboðslínur ... quotedetails                          | SalesQuotationLineCommon Data ServiceEining            | QuoteDetails                                 | |
| Sölureikningshausar V2 ... invoices                                               | SalesInvoiceHeaderV2Entity                             | reikningur                                      | |
| Sölureikningslínur V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Vörpunarsértækar athugasemdir

1. Vegna sjálfsábyrgðar gætirðu þurft að keyra fyrstu samstillingu tvisvar.
2. Sjálfgefið er að slökkt er á fyrstu samstillingu vegna yfir-/undirvensla („snjöll“ pöntun er ekki meðhöndluð af verkvanginum). Þess vegna verður að samstilla núverandi vöruflokka handvirkt (til dæmis með því að uppfæra lýsingu á flokknum) í réttri röð (rótarflokkur fyrst, síðan undirflokkar og síðan undirflokkar undirflokka). Farðu í **Afurðaupplýsingastjórnun \> Uppsetning \> Tegundir og eigindir \> Tegundastigveldi**. Á síðunni **Tegundastigveldi** er hægt að velja hvert stigveldi og sjá vöruflokka í því.
3. Vörpun á tómum leitarreitum **ItemNumberInLocation** og fyrstu, önnur og þriðju aukalegu vöruhúsasvæðin munu valda því að upphafleg samstilling tekt ekki. Þess vegna eru þessar varpanir fjarlægðar í bili.
4. Vörpun á tómum reit **CaptureWeight** veldur því að upphafleg samstilling tekst ekki. Þess vegna er þessi vörpun fjarlægð í bili.

### <a name="setup-related-information"></a>Uppsetningartengdar upplýsingar

+ Þegar færslur eru fyrst stofnaðar í einingunni **Afurðir** í líkanadrifnum forritum í Dynamics 365 hafa þær stöðuna **Drög**. Til að breyta stöðunni í **Virkt** ferðu í **Stillingar \> Stjórnun \> Kerfistillingar \> Sala** í líkanadrifna forritinu og stillir valkostinn **Stofna afurðir í virkri stöðu** á **Já**.
+ Ef þú býrð til skrár í einingunni **Afurðir** í líkanadrifnum forritum í Dynamics 365 eða í Common Data Service áður en þú virkjar tvíritun, verða þessar skrár aðeins uppfærðar ef allur lykillinn, þ.m.t. **Fyrirtæki**, samsvarar gögnum í forriti Finance and Operations.
+ Samstilling á Einingunni **Vörur** er einátta, úr forritum Finance and Operations til Common Data Service. Ef varpaður reitur í einingunni **Vörur** í líkanadrifnum forritum í Dynamics 365 er uppfærður verður uppfærslan yfirskrifuð við næstu samstillingu úr forritinu Finance and Operations.

### <a name="known-issues"></a>Þekkt vandamál

- Villa kemur upp þegar einingu er eytt í forriti Finance and Operations. Þegar mælieiningar eru samstilltar úr forriti Finance and Operations til Common Data Service verður fyrsta einingin í tilteknum flokki stofnuð sem frumeiningin og kemur í veg fyrir eyðingu.

    **Mótvægisaðgerðir:** Eyddu fyrst einingunni í Common Data Service. Það er síðan hægt að eyða í forritinu Finance and Operations.

- Villa kemur upp þegar rekstrarsvæði er eytt í Common Data Service. Villuboðin segja: „Infolog: Viðvörun: Ekki er hægt að eyða aðalnetfangi; Viðvörun: Ekki var hægt að eyða færslunni vegna þess að staðfesting mistókst fyrir eftirfarandi gagnaheimild: InventSiteLogisticsLocation (InventSiteLogisticsLocation).“ Þessi villa stafar af vandamáli í gagnaeiningunni í forritinu Finance and Operations.

    **Mótvægisaðgerðir:** Þú getur eytt síðunni í forritinu Finance and Operations. Síðunni verður síðan eytt í Common Data Service ef samsvarandi tvískipt kort er í gangi.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance einingar

Eftirfarandi einingar fyrir Dynamics 365 Finance eru skráðar í þeirri röð sem ætti að virkja þær.

| Heiti vörpunar á síðunni Tvíritun | Heiti lýsigagna einingar í Finance | Heiti lýsigagna einingar í Common Data Service | Athugasemdir |
|---|---|---|---|
| Gjaldmiðlar ... transactioncurrencies                                            | CurrencyEntity                              | Gjaldmiðill                                   | |
| Gerð gengis ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Gjaldmiðlapar gengis ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service gengi ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEining       | msdyn_currencyexchangerate                 | Sjá [athugasemd 1](#fin-notes). |
| Samþættingareining fjárhagsdagatals ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Samþættingareining fjárhagsdagatalsárs ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Tímabil fjárhagstímabils ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Gerð stigveldis fyrirtækis ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Sjá [athugasemd 1](#fin-notes). |
| Tilgangur fyrir stigveldi fyrirtækis ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Sjá [athugasemd 1](#fin-notes). |
| Lögaðilar ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Sjá [athugasemd 1](#fin-notes). |
| Lögaðilar ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Rekstrareining ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Sjá [athugasemd 1](#fin-notes). |
| Stigveldi fyrirtækis - birt ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Sjá [athugasemd 1](#fin-notes). |
| Viðskeyti nafna ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Greiðsludagar Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Greiðsludagalínur Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Greiðsluáætlun ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Greiðsluáætlunarlínur ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Greiðsluskilmálar ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Greiðslumáti viðskiptavinar ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Greiðslumáti lánardrottins ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Flokkar viðskiptavina ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Lánardrottnaflokkar ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| VSK-flokkar ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| VSK-flokkar vöru ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Fjárhagsbókunarflokkar virðisaukaskatts V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Eining undanþágukóða virðisaukaskatts fyrir Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Skattayfirvöld ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| VSK-kóði ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Sjá [athugasemd 1](#fin-notes). |
| Fjárhagsvíddarsnið ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Fjárhagsvíddir ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Staðgreiðsluskattsflokkar ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Staðgreiðsluskattskóðar ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Bókhaldslykill ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Fjárhagur ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Sjá [athugasemd 1](#fin-notes). |
| Flokkar aðallykla ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Aðallykill ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Viðskiptavinir V3 ... accounts                                                       | CustCustomerV3Entity                        | lykill                                    | Sjá [athugasemd 2](#fin-notes). |
| Viðskiptavinir V3 ... contacts                                                       | CustCustomerV3Entity                        | tengiliður                                    | Sjá [athugasemd 3](#fin-notes). |
| Lánardrottnar V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Sjá [athugasemd 2](#fin-notes). |
| Common Data Service tengiliðir V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | tengiliður                                    | Sjá [athugasemd 4](#fin-notes). |
| Common Data Service tengiliðir V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | tengiliður                                    | Sjá [athugasemd 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Vörpunarsértækar athugasemdir

1. Einstefnusamstilling á sér stað úr forritum Finance and Operations í Common Data Service.
2. Vegna sjálfsábyrgðar gætirðu þurft að keyra fyrstu samstillingu oftar en einu sinni. Passaðu að velja **Viðskiptavinur** sem venslagerð þegar þú stofnar lykil með síðunni **Lyklar** í Common Data Service. Ef þú lendir í vandræðum með reitinn **Aðaltengiliður** við fyrstu samstillingu, fjarlægðu þann reit úr vörpuninni og keyrðu síðan fyrstu samstillingu aftur. Eftir að fyrstu samstillingu er lokið skaltu stöðva vörpunina og bæta reitnum **Aðaltengiliður** aftur við hana. Ræstu vörpunina síðan aftur en slepptu fyrstu samstillingu. Gildið í reitnum **Aðaltengiliður** verður ekki með í fyrstu samstillingu og þú verður að flytja gildin handvirkt.
3. Passaðu að stilla valkostinn **Seljanlegt** á **Já** á síðunni **Tengiliðir** í Common Data Service þegar þú reynir að stofna viðskiptavini af gerðinni **Einstaklingur**.
4. Þessi vörpun er með síu á báðum hliðum til að tengja tengiliði viðskiptavina. Opnaðu vörpunarupplýsingarnar, veldu síuhnappinn (trektartáknið) við hliðina á einingaheitinu **Sales.Contact** og passaðu að skráarskilyrðin innihald **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Þessi vörpun er með síu á báðum hliðum til að tengja tengiliði lánardrottna. Opnaðu vörpunarupplýsingarnar, veldu síuhnappinn (trektartáknið) við hliðina á einingaheitinu **Sales.Contact** og passaðu að síuskilyrðin innihald **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources einingar

Eftirfarandi einingar fyrir Dynamics 365 Human Resources eru skráðar í þeirri röð sem ætti að virkja þær.

| Heiti vörpunar á síðunni Tvíritun | Heiti lýsigagna einingar í Human Resources | Heiti lýsigagna einingar í Common Data Service | Athugasemdir |
|---|---|---|---|
| cdm_jobfunction - Starfshlutverk                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - Atvinnugerðir                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - Störf                                               |                                   | cdm_jobs                         | |
| cdm_jobs - Upplýsingar um starf                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - Gerð stöðu                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Grunnstaða                              | HcmPositionBaseEntity             | cdm_jobposition                  | Sjá [athugasemd 1](#hr-notes). |
| cdm_jobposition - Upplýsingar um stöðu                            | HcmPositionDetailEntity           | cdm_jobposition                  | Sjá [athugasemd 1](#hr-notes). |
| cdm_jobposition - Lengd stöðu                           | HcmPositionDurationEntity         | cdm_jobposition                  | Sjá [athugasemd 1](#hr-notes). |
| cdm_jobposition - Stöðustigveldi                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Sjá [athugasemd 1](#hr-notes). |
| cdm_veteranstatus - Uppgjafahermaður                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - Þjóðlegur uppruni                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - Tungumálakóði                              |                                   | cdm_languagecode                 | |
| cdm_worker - Starfskraftur                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - Atvinna                                 |                                   | cdm_employments                  | |
| cdm_employments - Upplýsingar um atvinnu                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Stöðuúthlutun starfskrafts | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Sjá [athugasemd 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Vörpunarsértækar athugasemdir

1. Einni Common Data Service einingu er varpað á nokkrar forritseiningar Finance and Operations.
2. Þessi vörpun hefur sjálfstilvísun.

## <a name="asset-management-entities"></a>Einingar eignastýringar

Eftirfarandi einingar fyrir eignastýringu fyrir Dynamics 365 Supply Chain Management eru skráðar í þeirri röð sem ætti að virkja þær.

| Heiti vörpunar á síðunni Tvíritun | Heiti lýsigagna einingar í eignastýringu | Heiti lýsigagna einingar í Common Data Service | Athugasemdir |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Líftímastöður eigna í eignastýringu               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Líftímalíkön eigna í eignastýringu               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Líftímalíkön virkra staðsetninga eignastýringar | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Líftímastöður virkra staðsetninga eignastýringar | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Eignagerðir eignastýringar                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Virkar staðsetningagerðir eignastýringar            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Virkar staðsetningar eignastýringar                 | msdyn_functionallocations                | Sjá [athugasemdina](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Eignir eignastýringar                               | msdyn_customerassets                     | Sjá [athugasemdina](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Framleiðendur eignastýringar                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Líkön eignastýringar                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Ábyrgð eignastýringar                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Vörpunarsértækar athugasemdir

- Vegna sjálfsábyrgðar gætirðu þurft að keyra fyrstu samstillingu oftar en einu sinni.
