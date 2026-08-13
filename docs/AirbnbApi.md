# \AirbnbApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**airbnb_airbnb_scraper_health_check**](AirbnbApi.md#airbnb_airbnb_scraper_health_check) | **GET** /v1/airbnb/health | Airbnb scraper health check
[**airbnb_airbnb_scraper_health_check_head**](AirbnbApi.md#airbnb_airbnb_scraper_health_check_head) | **HEAD** /v1/airbnb/health | Airbnb scraper health check
[**airbnb_get_availability_calendar**](AirbnbApi.md#airbnb_get_availability_calendar) | **GET** /v1/airbnb/listings/{room_id}/calendar | Get availability calendar
[**airbnb_get_experience_detail**](AirbnbApi.md#airbnb_get_experience_detail) | **GET** /v1/airbnb/experiences/{experience_id} | Get experience detail
[**airbnb_get_listing_detail**](AirbnbApi.md#airbnb_get_listing_detail) | **GET** /v1/airbnb/listings/{room_id} | Get listing detail
[**airbnb_get_listing_reviews**](AirbnbApi.md#airbnb_get_listing_reviews) | **GET** /v1/airbnb/listings/{room_id}/reviews | Get listing reviews
[**airbnb_search_experiences**](AirbnbApi.md#airbnb_search_experiences) | **GET** /v1/airbnb/experiences | Search experiences
[**airbnb_search_stays**](AirbnbApi.md#airbnb_search_stays) | **GET** /v1/airbnb/search | Search stays



## airbnb_airbnb_scraper_health_check

> serde_json::Value airbnb_airbnb_scraper_health_check()
Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

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


## airbnb_airbnb_scraper_health_check_head

> serde_json::Value airbnb_airbnb_scraper_health_check_head()
Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

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


## airbnb_get_availability_calendar

> serde_json::Value airbnb_get_availability_calendar(room_id, month, year, months, currency, locale)
Get availability calendar

Day-by-day availability for up to 12 months: bookable, check-in/out windows and min/max nights per date.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**room_id** | **String** |  | [required] |
**month** | Option<**i32**> | Start month (1-12) |  |[default to 1]
**year** | Option<**i32**> | Start year |  |[default to 2026]
**months** | Option<**i32**> | Number of months (max 12) |  |[default to 12]
**currency** | Option<**String**> |  |  |
**locale** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## airbnb_get_experience_detail

> serde_json::Value airbnb_get_experience_detail(experience_id, adults, children, infants, currency, locale)
Get experience detail

Full detail for one experience: description, rating, host, location and photos.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**experience_id** | **String** |  | [required] |
**adults** | Option<**i32**> |  |  |[default to 1]
**children** | Option<**i32**> |  |  |[default to 0]
**infants** | Option<**i32**> |  |  |[default to 0]
**currency** | Option<**String**> |  |  |
**locale** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## airbnb_get_listing_detail

> serde_json::Value airbnb_get_listing_detail(room_id, adults, currency, locale)
Get listing detail

Full detail for one listing: amenities, house rules, host, ratings, coordinates and photos.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**room_id** | **String** |  | [required] |
**adults** | Option<**i32**> |  |  |[default to 1]
**currency** | Option<**String**> |  |  |
**locale** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## airbnb_get_listing_reviews

> serde_json::Value airbnb_get_listing_reviews(room_id, limit, offset, sort, currency, locale)
Get listing reviews

Paginated guest reviews with reviewer, rating, date, text and host response.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**room_id** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 24]
**offset** | Option<**i32**> |  |  |[default to 0]
**sort** | Option<**String**> | MOST_RECENT | RATING_DESC | RATING_ASC |  |[default to MOST_RECENT]
**currency** | Option<**String**> |  |  |
**locale** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## airbnb_search_experiences

> serde_json::Value airbnb_search_experiences(location, cursor, currency, locale)
Search experiences

Search Airbnb Experiences by location.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | **String** | Free-text place, e.g. 'Rome, Italy' | [required] |
**cursor** | Option<**String**> | next_page_cursor from a prior response |  |
**currency** | Option<**String**> |  |  |
**locale** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## airbnb_search_stays

> serde_json::Value airbnb_search_stays(location, ne_lat, ne_lng, sw_lat, sw_lng, check_in, check_out, adults, children, infants, pets, price_min, price_max, min_bedrooms, min_beds, min_bathrooms, room_type, cursor, limit, currency, locale)
Search stays

Search Airbnb stays by place name and/or map bounding box, with dates, guests, price and property filters. Paginate with the `cursor`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location** | Option<**String**> | Free-text place, e.g. 'Paris, France' |  |
**ne_lat** | Option<**f64**> | Map bounding-box NE latitude |  |
**ne_lng** | Option<**f64**> | Map bounding-box NE longitude |  |
**sw_lat** | Option<**f64**> | Map bounding-box SW latitude |  |
**sw_lng** | Option<**f64**> | Map bounding-box SW longitude |  |
**check_in** | Option<**String**> | Check-in date YYYY-MM-DD |  |
**check_out** | Option<**String**> | Check-out date YYYY-MM-DD |  |
**adults** | Option<**i32**> |  |  |[default to 1]
**children** | Option<**i32**> |  |  |[default to 0]
**infants** | Option<**i32**> |  |  |[default to 0]
**pets** | Option<**i32**> |  |  |[default to 0]
**price_min** | Option<**i32**> |  |  |
**price_max** | Option<**i32**> |  |  |
**min_bedrooms** | Option<**i32**> |  |  |
**min_beds** | Option<**i32**> |  |  |
**min_bathrooms** | Option<**i32**> |  |  |
**room_type** | Option<**String**> | e.g. 'Entire home/apt', 'Private room' |  |
**cursor** | Option<**String**> | next_page_cursor from a prior response |  |
**limit** | Option<**i32**> |  |  |[default to 18]
**currency** | Option<**String**> | ISO currency, e.g. USD, EUR |  |
**locale** | Option<**String**> | Locale, e.g. en, fr |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

