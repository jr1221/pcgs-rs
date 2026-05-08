# \PcgsPublicApiMethodsApi

All URIs are relative to *https://api.pcgs.com/publicapi*

Method | HTTP request | Description
------------- | ------------- | -------------
[**banknote_get_banknote_by_cert_no**](PcgsPublicApiMethodsApi.md#banknote_get_banknote_by_cert_no) | **GET** /banknotedetail/GetBanknoteByCertNo | Get Banknote infos
[**banknote_get_banknote_by_grade**](PcgsPublicApiMethodsApi.md#banknote_get_banknote_by_grade) | **GET** /banknotedetail/GetBanknoteByGrade | Get Banknote infos By Grade and SpecNo
[**banknote_get_banknote_images_by_cert_no**](PcgsPublicApiMethodsApi.md#banknote_get_banknote_images_by_cert_no) | **GET** /banknotedetail/GetBanknoteImagesByCertNo | 
[**coin_detail_get_aprby_barcode**](PcgsPublicApiMethodsApi.md#coin_detail_get_aprby_barcode) | **GET** /coindetail/GetAPRByBarcode | Get Auction Prices Realized data for a coin using its holder's barcode
[**coin_detail_get_aprby_cert_no**](PcgsPublicApiMethodsApi.md#coin_detail_get_aprby_cert_no) | **GET** /coindetail/GetAPRByCertNo/{CertNo} | Get Auction Prices Realized data for a coin using its cert number
[**coin_detail_get_aprby_grade**](PcgsPublicApiMethodsApi.md#coin_detail_get_aprby_grade) | **GET** /coindetail/GetAPRByGrade | Get Auction Prices Realized data for a coin using its PCGS number and grade
[**coin_detail_get_coin_facts_by_barcode**](PcgsPublicApiMethodsApi.md#coin_detail_get_coin_facts_by_barcode) | **GET** /coindetail/GetCoinFactsByBarcode | Get CoinFacts data for a coin using its holder's barcode
[**coin_detail_get_coin_facts_by_cert_no**](PcgsPublicApiMethodsApi.md#coin_detail_get_coin_facts_by_cert_no) | **GET** /coindetail/GetCoinFactsByCertNo/{certNo} | Get CoinFacts data for a coin using its cert number
[**coin_detail_get_coin_facts_by_grade**](PcgsPublicApiMethodsApi.md#coin_detail_get_coin_facts_by_grade) | **GET** /coindetail/GetCoinFactsByGrade | Get CoinFacts data for a coin using its PCGS number and grade
[**coin_detail_get_images_by_cert_no**](PcgsPublicApiMethodsApi.md#coin_detail_get_images_by_cert_no) | **GET** /coindetail/GetImagesByCertNo | Get All PCGS Images available for the certification number
[**order_get_orders_by_date_range**](PcgsPublicApiMethodsApi.md#order_get_orders_by_date_range) | **GET** /orderdetail/GetOrdersByDateRange | Get the PCGS orders from a specified date range using the order received date
[**order_get_orders_by_submission_no**](PcgsPublicApiMethodsApi.md#order_get_orders_by_submission_no) | **GET** /orderdetail/GetOrdersBySubmissionNo | Get the PCGS orders based off the account used to register for the API



## banknote_get_banknote_by_cert_no

> models::BanknoteModel banknote_get_banknote_by_cert_no(cert_no, language_code)
Get Banknote infos

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**cert_no** | **String** | The PCGS certificate number | [required] |
**language_code** | Option<**String**> | The PCGS certificate number |  |

### Return type

[**models::BanknoteModel**](BanknoteModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## banknote_get_banknote_by_grade

> models::BanknotesModel banknote_get_banknote_by_grade(pcgs_no, grade_no)
Get Banknote infos By Grade and SpecNo

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**pcgs_no** | **String** | The PCGS Spec No | [required] |
**grade_no** | **i32** | The PCGS Grade | [required] |

### Return type

[**models::BanknotesModel**](BanknotesModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## banknote_get_banknote_images_by_cert_no

> models::ImageModel banknote_get_banknote_images_by_cert_no(cert_no)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**cert_no** | **String** |  | [required] |

### Return type

[**models::ImageModel**](ImageModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## coin_detail_get_aprby_barcode

> models::CoinFactsModel coin_detail_get_aprby_barcode(barcode, grading_service, start_date, end_date)
Get Auction Prices Realized data for a coin using its holder's barcode

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**barcode** | **String** | The barcode text captured from either a PCGS/NGC holder | [required] |
**grading_service** | **String** | The grading service. Possible values are PCGS and NGC | [required] |
**start_date** | Option<**String**> | The starting date of auction items to retrieve in mm-dd-yyyy format |  |
**end_date** | Option<**String**> | The ending date of auction items to retrieve in mm-dd-yyyy format |  |

### Return type

[**models::CoinFactsModel**](CoinFactsModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## coin_detail_get_aprby_cert_no

> models::AuctionModel coin_detail_get_aprby_cert_no(cert_no)
Get Auction Prices Realized data for a coin using its cert number

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**cert_no** | **String** | The PCGS cert number | [required] |

### Return type

[**models::AuctionModel**](AuctionModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## coin_detail_get_aprby_grade

> models::AuctionListModel coin_detail_get_aprby_grade(pcgsno, grade_no, plus_grade, start_date, end_date, number_of_records)
Get Auction Prices Realized data for a coin using its PCGS number and grade

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**pcgsno** | **String** | The PCGS number of the coin | [required] |
**grade_no** | **i32** | The grade number | [required] |
**plus_grade** | **bool** | Set to true if it’s a plus grade, false if not | [required] |
**start_date** | Option<**String**> | The starting date of auction items to retrieve in mm-dd-yyyy format |  |
**end_date** | Option<**String**> | The ending date of auction items to retrieve in mm-dd-yyyy format |  |
**number_of_records** | Option<**i32**> | How many auction records to return.  Default is 100 |  |

### Return type

[**models::AuctionListModel**](AuctionListModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## coin_detail_get_coin_facts_by_barcode

> models::CoinFactsByBarcodeModel coin_detail_get_coin_facts_by_barcode(barcode, grading_service)
Get CoinFacts data for a coin using its holder's barcode

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**barcode** | **String** | The barcode text captured from either a PCGS/NGC holder | [required] |
**grading_service** | **String** | The grading service. Possible values are PCGS and NGC | [required] |

### Return type

[**models::CoinFactsByBarcodeModel**](CoinFactsByBarcodeModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## coin_detail_get_coin_facts_by_cert_no

> models::CoinFactsModel coin_detail_get_coin_facts_by_cert_no(cert_no, retrieve_all_data)
Get CoinFacts data for a coin using its cert number

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**cert_no** | **String** | The PCGS cert number | [required] |
**retrieve_all_data** | Option<**bool**> | Set to true (default) will return all CoinFacts data including Images, APR, Pop, &amp; Prices.  Set to false if you want to exclude getting APR, Pop, Images, &amp; Prices. |  |

### Return type

[**models::CoinFactsModel**](CoinFactsModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## coin_detail_get_coin_facts_by_grade

> models::CoinFactsByGradeModel coin_detail_get_coin_facts_by_grade(pcgsno, grade_no, plus_grade)
Get CoinFacts data for a coin using its PCGS number and grade

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**pcgsno** | **String** | The PCGS number of the coin | [required] |
**grade_no** | **i32** | The grade number | [required] |
**plus_grade** | **bool** | Set to true if it’s a plus grade, false if not | [required] |

### Return type

[**models::CoinFactsByGradeModel**](CoinFactsByGradeModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## coin_detail_get_images_by_cert_no

> models::ImageModel coin_detail_get_images_by_cert_no(cert_no)
Get All PCGS Images available for the certification number

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**cert_no** | **String** | The PCGS certificate number | [required] |

### Return type

[**models::ImageModel**](ImageModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## order_get_orders_by_date_range

> models::OrderModel order_get_orders_by_date_range(start_date, end_date, page_no, page_size)
Get the PCGS orders from a specified date range using the order received date

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**start_date** | **String** | The start date in mm-dd-yyyy format | [required] |
**end_date** | **String** | The end date in mm-dd-yyyy format | [required] |
**page_no** | Option<**i32**> | The page to return |  |
**page_size** | Option<**i32**> | The number of orders returned per page.  Default is 10 |  |

### Return type

[**models::OrderModel**](OrderModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## order_get_orders_by_submission_no

> models::OrderModel order_get_orders_by_submission_no(submission_no)
Get the PCGS orders based off the account used to register for the API

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**submission_no** | **String** | The submission number of the order.  It will return a list of orders if the submission number has been submitted multiple times | [required] |

### Return type

[**models::OrderModel**](OrderModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

