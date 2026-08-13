# \TikTokApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tiktok_general_search**](TikTokApi.md#tiktok_general_search) | **GET** /v1/tiktok/search | General search
[**tiktok_get_comment_replies**](TikTokApi.md#tiktok_get_comment_replies) | **GET** /v1/tiktok/comments/{comment_id}/replies | Get comment replies
[**tiktok_get_comments**](TikTokApi.md#tiktok_get_comments) | **GET** /v1/tiktok/videos/{video_id}/comments | Get comments
[**tiktok_get_followers_deprecated**](TikTokApi.md#tiktok_get_followers_deprecated) | **GET** /v1/tiktok/users/{username}/followers | Get followers (deprecated)
[**tiktok_get_following_deprecated**](TikTokApi.md#tiktok_get_following_deprecated) | **GET** /v1/tiktok/users/{username}/following | Get following (deprecated)
[**tiktok_get_hashtag_detail**](TikTokApi.md#tiktok_get_hashtag_detail) | **GET** /v1/tiktok/hashtags/{name} | Get hashtag detail
[**tiktok_get_hashtag_videos**](TikTokApi.md#tiktok_get_hashtag_videos) | **GET** /v1/tiktok/hashtags/{name}/videos | Get hashtag videos
[**tiktok_get_liked_videos_deprecated**](TikTokApi.md#tiktok_get_liked_videos_deprecated) | **GET** /v1/tiktok/users/{username}/liked | Get liked videos (deprecated)
[**tiktok_get_music_sound_detail**](TikTokApi.md#tiktok_get_music_sound_detail) | **GET** /v1/tiktok/music/{music_id} | Get music/sound detail
[**tiktok_get_music_videos**](TikTokApi.md#tiktok_get_music_videos) | **GET** /v1/tiktok/music/{music_id}/videos | Get music videos
[**tiktok_get_oembed_metadata**](TikTokApi.md#tiktok_get_oembed_metadata) | **GET** /v1/tiktok/oembed | Get oEmbed metadata
[**tiktok_get_related_videos**](TikTokApi.md#tiktok_get_related_videos) | **GET** /v1/tiktok/videos/{video_id}/related | Get related videos
[**tiktok_get_reposts**](TikTokApi.md#tiktok_get_reposts) | **GET** /v1/tiktok/users/{username}/reposts | Get reposts
[**tiktok_get_tiktok_ad_detail**](TikTokApi.md#tiktok_get_tiktok_ad_detail) | **GET** /v1/tiktok/ads/{ad_id} | Get TikTok ad detail
[**tiktok_get_transcript**](TikTokApi.md#tiktok_get_transcript) | **GET** /v1/tiktok/videos/{video_id}/transcript | Get transcript
[**tiktok_get_user_profile**](TikTokApi.md#tiktok_get_user_profile) | **GET** /v1/tiktok/users/{username} | Get user profile
[**tiktok_get_user_videos**](TikTokApi.md#tiktok_get_user_videos) | **GET** /v1/tiktok/users/{username}/videos | Get user videos
[**tiktok_get_video_detail**](TikTokApi.md#tiktok_get_video_detail) | **GET** /v1/tiktok/videos/{video_id} | Get video detail
[**tiktok_health_check**](TikTokApi.md#tiktok_health_check) | **GET** /v1/tiktok/health | Health check
[**tiktok_health_check_head**](TikTokApi.md#tiktok_health_check_head) | **HEAD** /v1/tiktok/health | Health check
[**tiktok_list_regions**](TikTokApi.md#tiktok_list_regions) | **GET** /v1/tiktok/regions | List regions
[**tiktok_search_hashtags**](TikTokApi.md#tiktok_search_hashtags) | **GET** /v1/tiktok/search/hashtags | Search hashtags
[**tiktok_search_the_tiktok_ad_library**](TikTokApi.md#tiktok_search_the_tiktok_ad_library) | **GET** /v1/tiktok/ads/search | Search the TikTok Ad Library
[**tiktok_search_tiktok_advertisers**](TikTokApi.md#tiktok_search_tiktok_advertisers) | **GET** /v1/tiktok/ads/advertisers | Search TikTok advertisers
[**tiktok_search_users**](TikTokApi.md#tiktok_search_users) | **GET** /v1/tiktok/search/users | Search users
[**tiktok_search_videos**](TikTokApi.md#tiktok_search_videos) | **GET** /v1/tiktok/search/videos | Search videos
[**tiktok_trending_hashtags**](TikTokApi.md#tiktok_trending_hashtags) | **GET** /v1/tiktok/trending/hashtags | Trending hashtags
[**tiktok_trending_songs**](TikTokApi.md#tiktok_trending_songs) | **GET** /v1/tiktok/trending/songs | Trending songs
[**tiktok_trending_videos**](TikTokApi.md#tiktok_trending_videos) | **GET** /v1/tiktok/trending/videos | Trending videos



## tiktok_general_search

> serde_json::Value tiktok_general_search(query, region, count, cursor)
General search

General TikTok search — video results from the Top feed.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keyword | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_comment_replies

> serde_json::Value tiktok_get_comment_replies(comment_id, video_id, region, count, cursor)
Get comment replies

Get replies to a TikTok comment (best-effort).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**comment_id** | **String** |  | [required] |
**video_id** | **String** | Parent video id | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> | Pagination cursor from a prior page's pagination.cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_comments

> serde_json::Value tiktok_get_comments(video_id, region, count, cursor)
Get comments

Get top-level comments on a TikTok video.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> | Pagination cursor from a prior page's pagination.cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_followers_deprecated

> serde_json::Value tiktok_get_followers_deprecated(username, region, count)
Get followers (deprecated)

DEPRECATED — TikTok followers require an authenticated account session. Returns HTTP 410.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 30]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_following_deprecated

> serde_json::Value tiktok_get_following_deprecated(username, region, count)
Get following (deprecated)

DEPRECATED — TikTok following requires an authenticated account session. Returns HTTP 410.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 30]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_hashtag_detail

> serde_json::Value tiktok_get_hashtag_detail(name, region)
Get hashtag detail

Get TikTok hashtag/challenge detail.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**name** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_hashtag_videos

> serde_json::Value tiktok_get_hashtag_videos(name, region, count, cursor)
Get hashtag videos

Get videos tagged with a TikTok hashtag.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**name** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 30]
**cursor** | Option<**String**> | Pagination cursor from a prior page's pagination.cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_liked_videos_deprecated

> serde_json::Value tiktok_get_liked_videos_deprecated(username, region, count)
Get liked videos (deprecated)

DEPRECATED — TikTok liked videos require an authenticated account session. Returns HTTP 410.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 30]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_music_sound_detail

> serde_json::Value tiktok_get_music_sound_detail(music_id, region)
Get music/sound detail

Get TikTok sound/music detail.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**music_id** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_music_videos

> serde_json::Value tiktok_get_music_videos(music_id, region, count, cursor)
Get music videos

Get videos using a given TikTok sound.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**music_id** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 30]
**cursor** | Option<**String**> | Pagination cursor from a prior page's pagination.cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_oembed_metadata

> serde_json::Value tiktok_get_oembed_metadata(url, region)
Get oEmbed metadata

Get cheap unauthenticated oEmbed metadata for a TikTok URL.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | Full TikTok video or profile URL | [required] |
**region** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_related_videos

> serde_json::Value tiktok_get_related_videos(video_id, region, count)
Get related videos

Get TikTok's related videos for a given video.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 16]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_reposts

> serde_json::Value tiktok_get_reposts(username, region, count)
Get reposts

Get videos a TikTok user has reposted.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 30]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_tiktok_ad_detail

> serde_json::Value tiktok_get_tiktok_ad_detail(ad_id, region)
Get TikTok ad detail

Get a single ad's advertiser, creatives, and targeting/impression breakdown.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |
**region** | Option<**String**> | EU region code (the Ad Library is EU-only) |  |[default to DE]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_transcript

> serde_json::Value tiktok_get_transcript(video_id, region)
Get transcript

Get subtitle/caption tracks for a TikTok video.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_user_profile

> serde_json::Value tiktok_get_user_profile(username, region)
Get user profile

Get a TikTok user's full profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**region** | Option<**String**> | Content region (ISO 3166-1 alpha-2) |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_user_videos

> serde_json::Value tiktok_get_user_videos(username, region, count, cursor)
Get user videos

Get a TikTok user's posted videos.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 30]
**cursor** | Option<**String**> | Pagination cursor from a prior page's `pagination.cursor` (signer path only). |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_get_video_detail

> serde_json::Value tiktok_get_video_detail(video_id, region, username)
Get video detail

Get full metadata for a single TikTok video/post.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**region** | Option<**String**> |  |  |[default to US]
**username** | Option<**String**> | Author handle (skips oEmbed lookup) |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_health_check

> serde_json::Value tiktok_health_check()
Health check

Check health of the TikTok scraper service.

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


## tiktok_health_check_head

> serde_json::Value tiktok_health_check_head()
Health check

Check health of the TikTok scraper service.

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


## tiktok_list_regions

> serde_json::Value tiktok_list_regions()
List regions

List supported TikTok content regions.

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


## tiktok_search_hashtags

> serde_json::Value tiktok_search_hashtags(query, region, count, cursor)
Search hashtags

Search TikTok hashtags by keyword.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keyword | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_search_the_tiktok_ad_library

> serde_json::Value tiktok_search_the_tiktok_ad_library(query, advertiser_id, region, days, sort, offset, search_id, count)
Search the TikTok Ad Library

Search TikTok's Commercial Content Library (ad transparency) by keyword or advertiser.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | Option<**String**> | Keyword (ignored when advertiser_id is set) |  |[default to ]
**advertiser_id** | Option<**String**> | Advertiser business id(s) for advertiser search |  |[default to ]
**region** | Option<**String**> | EU region code (the Ad Library is EU-only) |  |[default to DE]
**days** | Option<**i32**> |  |  |[default to 30]
**sort** | Option<**String**> |  |  |[default to last_shown_date,desc]
**offset** | Option<**i32**> |  |  |[default to 0]
**search_id** | Option<**String**> |  |  |[default to ]
**count** | Option<**i32**> |  |  |[default to 20]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_search_tiktok_advertisers

> serde_json::Value tiktok_search_tiktok_advertisers(query, region, count)
Search TikTok advertisers

Look up TikTok advertiser business ids by name (feeds ads/search?advertiser_id=).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Advertiser name (or partial) to look up | [required] |
**region** | Option<**String**> | EU region code (the Ad Library is EU-only) |  |[default to DE]
**count** | Option<**i32**> |  |  |[default to 10]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_search_users

> serde_json::Value tiktok_search_users(query, region, count, cursor)
Search users

Search TikTok users by keyword.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keyword | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_search_videos

> serde_json::Value tiktok_search_videos(query, region, count, cursor)
Search videos

Search TikTok videos by keyword.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keyword | [required] |
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_trending_hashtags

> serde_json::Value tiktok_trending_hashtags(region, period, count)
Trending hashtags

Get trending hashtags (mobile Discover surface — view_count + creators).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**region** | Option<**String**> |  |  |[default to US]
**period** | Option<**i32**> |  |  |[default to 7]
**count** | Option<**i32**> |  |  |[default to 20]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_trending_songs

> serde_json::Value tiktok_trending_songs(region, period, count)
Trending songs

Get trending songs/sounds (mobile hot-music feed — ranked by usage).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**region** | Option<**String**> |  |  |[default to US]
**period** | Option<**i32**> |  |  |[default to 7]
**count** | Option<**i32**> |  |  |[default to 20]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## tiktok_trending_videos

> serde_json::Value tiktok_trending_videos(region, count)
Trending videos

Get trending videos from the TikTok Explore feed.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**region** | Option<**String**> |  |  |[default to US]
**count** | Option<**i32**> |  |  |[default to 20]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

