# \YelpApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**yelp_list_markets**](YelpApi.md#yelp_list_markets) | **GET** /v1/yelp/markets | List markets
[**yelp_search_businesses**](YelpApi.md#yelp_search_businesses) | **GET** /v1/yelp/search | Search businesses



## yelp_list_markets

> models::YelpMarketsResponse yelp_list_markets()
List markets

Yelp sites this API verifiably searches. Free.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::YelpMarketsResponse**](YelpMarketsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## yelp_search_businesses

> models::YelpSearchResponse yelp_search_businesses(location, query, market, category, sort_by, price, features, page)
Search businesses

Ranked Yelp businesses for a location, with ads kept separate. 15 credits; empty results free.  Ten businesses per page, pages 1-11. Narrow the location, category or filters to reach more businesses. Business detail and reviews are not part of this API.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | **String** | Where to search, as typed into Yelp: city, neighbourhood, address or postcode. | [required] |
**query** | Option<**String**> | What to search for (e.g. pizza, plumbers). Optional when category is set. |  |
**market** | Option<**String**> | Yelp site to search; see /markets. |  |[default to us]
**category** | Option<**String**> | Yelp category alias, e.g. pizza, coffee, plumbing. |  |
**sort_by** | Option<**String**> |  |  |[default to recommended]
**price** | Option<**String**> | Comma-separated price levels 1-4 ($ to $$$$). |  |
**features** | Option<**String**> | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible. |  |
**page** | Option<**i32**> | 1-based page, ten businesses each; pages 1-11. |  |[default to 1]

### Return type

[**models::YelpSearchResponse**](YelpSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

