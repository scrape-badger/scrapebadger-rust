# \FacebookApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**facebook_browse_a_marketplace_category**](FacebookApi.md#facebook_browse_a_marketplace_category) | **GET** /v1/facebook/marketplace/category/{category} | Browse a Marketplace category
[**facebook_get_a_marketplace_item**](FacebookApi.md#facebook_get_a_marketplace_item) | **GET** /v1/facebook/marketplace/item/{item_id} | Get a Marketplace item
[**facebook_get_advertiser_page_info**](FacebookApi.md#facebook_get_advertiser_page_info) | **GET** /v1/facebook/ads/pages/{page_id} | Get advertiser page info
[**facebook_get_an_ad**](FacebookApi.md#facebook_get_an_ad) | **GET** /v1/facebook/ads/{ad_archive_id} | Get an ad
[**facebook_get_group_detail**](FacebookApi.md#facebook_get_group_detail) | **GET** /v1/facebook/groups/{group_id} | Get group detail
[**facebook_get_group_posts**](FacebookApi.md#facebook_get_group_posts) | **GET** /v1/facebook/groups/{group_id}/posts | Get group posts
[**facebook_get_page_detail**](FacebookApi.md#facebook_get_page_detail) | **GET** /v1/facebook/pages/{identifier} | Get page detail
[**facebook_get_page_posts**](FacebookApi.md#facebook_get_page_posts) | **GET** /v1/facebook/pages/{identifier}/posts | Get page posts
[**facebook_get_post_comments**](FacebookApi.md#facebook_get_post_comments) | **GET** /v1/facebook/posts/{post_id}/comments | Get post comments
[**facebook_get_post_detail**](FacebookApi.md#facebook_get_post_detail) | **GET** /v1/facebook/posts/{post_id} | Get post detail
[**facebook_get_profile_detail**](FacebookApi.md#facebook_get_profile_detail) | **GET** /v1/facebook/profiles/{identifier} | Get profile detail
[**facebook_get_profile_posts**](FacebookApi.md#facebook_get_profile_posts) | **GET** /v1/facebook/profiles/{identifier}/posts | Get profile posts
[**facebook_list_categories**](FacebookApi.md#facebook_list_categories) | **GET** /v1/facebook/marketplace/categories | List categories
[**facebook_list_locations**](FacebookApi.md#facebook_list_locations) | **GET** /v1/facebook/marketplace/locations | List locations
[**facebook_search_advertiser_pages**](FacebookApi.md#facebook_search_advertiser_pages) | **GET** /v1/facebook/ads/pages/search | Search advertiser pages
[**facebook_search_events**](FacebookApi.md#facebook_search_events) | **GET** /v1/facebook/search/events | Search events
[**facebook_search_everything**](FacebookApi.md#facebook_search_everything) | **GET** /v1/facebook/search | Search everything
[**facebook_search_groups**](FacebookApi.md#facebook_search_groups) | **GET** /v1/facebook/search/groups | Search groups
[**facebook_search_marketplace**](FacebookApi.md#facebook_search_marketplace) | **GET** /v1/facebook/marketplace/search | Search Marketplace
[**facebook_search_pages**](FacebookApi.md#facebook_search_pages) | **GET** /v1/facebook/search/pages | Search Pages
[**facebook_search_people**](FacebookApi.md#facebook_search_people) | **GET** /v1/facebook/search/people | Search people
[**facebook_search_places**](FacebookApi.md#facebook_search_places) | **GET** /v1/facebook/search/places | Search places
[**facebook_search_posts**](FacebookApi.md#facebook_search_posts) | **GET** /v1/facebook/search/posts | Search posts
[**facebook_search_the_ad_library**](FacebookApi.md#facebook_search_the_ad_library) | **GET** /v1/facebook/ads/search | Search the Ad Library



## facebook_browse_a_marketplace_category

> serde_json::Value facebook_browse_a_marketplace_category(category, location, min_price, max_price, sort_by, after)
Browse a Marketplace category

Browse Marketplace listings in a category (vehicles, electronics, ...).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category** | **String** |  | [required] |
**location** | Option<**String**> |  |  |[default to nyc]
**min_price** | Option<**i32**> |  |  |
**max_price** | Option<**i32**> |  |  |
**sort_by** | Option<**String**> |  |  |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_a_marketplace_item

> serde_json::Value facebook_get_a_marketplace_item(item_id)
Get a Marketplace item

Get full detail for a single Marketplace listing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**item_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_advertiser_page_info

> serde_json::Value facebook_get_advertiser_page_info(page_id, country)
Get advertiser page info

Get advertiser page info: category, followers, page transparency (creation date, name history, managing organization, admin-account locations), related pages, and ad spend (for political/issue advertisers).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_id** | **String** |  | [required] |
**country** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_an_ad

> serde_json::Value facebook_get_an_ad(ad_archive_id, country)
Get an ad

Get a single Ad Library ad by its archive id. For EU/UK-targeted ads the response also includes transparency insights (payer/beneficiary, total EU reach, and age/gender/country reach breakdowns).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_archive_id** | **String** |  | [required] |
**country** | Option<**String**> | ISO country code (an EU code returns EU transparency) |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_group_detail

> serde_json::Value facebook_get_group_detail(group_id)
Get group detail

Get a Facebook group's details.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_group_posts

> serde_json::Value facebook_get_group_posts(group_id, after)
Get group posts

Get a Facebook group's post feed.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_page_detail

> serde_json::Value facebook_get_page_detail(identifier)
Get page detail

Get a Facebook Page's profile (name, category, followers, about).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**identifier** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_page_posts

> serde_json::Value facebook_get_page_posts(identifier, after)
Get page posts

Get a Facebook Page's timeline posts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**identifier** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_post_comments

> serde_json::Value facebook_get_post_comments(post_id, after, sort)
Get post comments

Get a Facebook post's comment thread (paginated).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**after** | Option<**String**> |  |  |
**sort** | Option<**String**> |  |  |[default to relevance]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_post_detail

> serde_json::Value facebook_get_post_detail(post_id)
Get post detail

Get a Facebook post's detail plus its top comments.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_profile_detail

> serde_json::Value facebook_get_profile_detail(identifier)
Get profile detail

Get a Facebook profile's details.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**identifier** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_get_profile_posts

> serde_json::Value facebook_get_profile_posts(identifier, after)
Get profile posts

Get a Facebook profile's timeline posts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**identifier** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_list_categories

> serde_json::Value facebook_list_categories()
List categories

List Marketplace category slugs (free).

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


## facebook_list_locations

> serde_json::Value facebook_list_locations()
List locations

List common Marketplace location slugs (free).

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


## facebook_search_advertiser_pages

> serde_json::Value facebook_search_advertiser_pages(query, country)
Search advertiser pages

Search advertiser Pages in the Ad Library — returns page ids, categories, likes/followers, verification and Instagram handles.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Advertiser name or keyword | [required] |
**country** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_events

> serde_json::Value facebook_search_events(q, after)
Search events

Search Facebook events.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_everything

> serde_json::Value facebook_search_everything(q, after)
Search everything

Global Facebook search (top results across pages, people, groups, posts).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_groups

> serde_json::Value facebook_search_groups(q, after)
Search groups

Search Facebook groups.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_marketplace

> serde_json::Value facebook_search_marketplace(query, location, min_price, max_price, days_since_listed, sort_by, item_condition, delivery_method, after)
Search Marketplace

Search Facebook Marketplace listings by keyword and location.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords | [required] |
**location** | Option<**String**> | Marketplace location slug |  |[default to nyc]
**min_price** | Option<**i32**> |  |  |
**max_price** | Option<**i32**> |  |  |
**days_since_listed** | Option<**i32**> |  |  |
**sort_by** | Option<**String**> |  |  |
**item_condition** | Option<**String**> |  |  |
**delivery_method** | Option<**String**> |  |  |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_pages

> serde_json::Value facebook_search_pages(q, after)
Search Pages

Search Facebook Pages.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_people

> serde_json::Value facebook_search_people(q, after)
Search people

Search Facebook profiles.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_places

> serde_json::Value facebook_search_places(q, after)
Search places

Search Facebook places.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_posts

> serde_json::Value facebook_search_posts(q, after)
Search posts

Search public Facebook posts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** |  | [required] |
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## facebook_search_the_ad_library

> serde_json::Value facebook_search_the_ad_library(query, country, ad_type, active_status, after)
Search the Ad Library

Search the Facebook Ad Library.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Advertiser or keyword | [required] |
**country** | Option<**String**> |  |  |[default to US]
**ad_type** | Option<**String**> |  |  |[default to all]
**active_status** | Option<**String**> |  |  |[default to active]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

