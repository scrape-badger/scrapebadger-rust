# \RufusApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**rufus_amazon_rufus_scraper_health_check**](RufusApi.md#rufus_amazon_rufus_scraper_health_check) | **GET** /v1/rufus/health | Amazon Rufus scraper health check
[**rufus_amazon_rufus_scraper_health_check_head**](RufusApi.md#rufus_amazon_rufus_scraper_health_check_head) | **HEAD** /v1/rufus/health | Amazon Rufus scraper health check
[**rufus_ask_amazon_rufus_a_question**](RufusApi.md#rufus_ask_amazon_rufus_a_question) | **GET** /v1/rufus/ask | Ask Amazon Rufus a question
[**rufus_ask_amazon_rufus_a_question_post**](RufusApi.md#rufus_ask_amazon_rufus_a_question_post) | **POST** /v1/rufus/ask | Ask Amazon Rufus a question (POST)
[**rufus_list_amazon_rufus_models**](RufusApi.md#rufus_list_amazon_rufus_models) | **GET** /v1/rufus/models | List Amazon Rufus models



## rufus_amazon_rufus_scraper_health_check

> serde_json::Value rufus_amazon_rufus_scraper_health_check()
Amazon Rufus scraper health check

Check health of the Amazon service that serves Rufus (accepts HEAD).

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rufus_amazon_rufus_scraper_health_check_head

> serde_json::Value rufus_amazon_rufus_scraper_health_check_head()
Amazon Rufus scraper health check

Check health of the Amazon service that serves Rufus (accepts HEAD).

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rufus_ask_amazon_rufus_a_question

> serde_json::Value rufus_ask_amazon_rufus_a_question(prompt, asin)
Ask Amazon Rufus a question

Ask Alexa for Shopping (Rufus) and get its answer and product cards.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prompt** | **String** | The shopping question to ask (max 4000 characters). | [required] |
**asin** | Option<**String**> | Optional product ASIN whose page should provide the shopping context. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rufus_ask_amazon_rufus_a_question_post

> serde_json::Value rufus_ask_amazon_rufus_a_question_post(rufus_ask_request)
Ask Amazon Rufus a question (POST)

POST form of `/ask`, accepting prompt and optional asin in the JSON body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rufus_ask_request** | [**RufusAskRequest**](RufusAskRequest.md) |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rufus_list_amazon_rufus_models

> serde_json::Value rufus_list_amazon_rufus_models()
List Amazon Rufus models

List the Amazon shopping assistant surface exposed by this API.

### Parameters

This endpoint does not need any parameter.

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

