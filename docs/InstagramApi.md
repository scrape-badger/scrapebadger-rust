# \InstagramApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**instagram_about_this_account**](InstagramApi.md#instagram_about_this_account) | **GET** /v1/instagram/users/{username}/about | About this account
[**instagram_blended_top_search**](InstagramApi.md#instagram_blended_top_search) | **GET** /v1/instagram/search/top | Blended top search
[**instagram_get_active_stories**](InstagramApi.md#instagram_get_active_stories) | **GET** /v1/instagram/users/{username}/stories | Get active stories
[**instagram_get_audio_track**](InstagramApi.md#instagram_get_audio_track) | **GET** /v1/instagram/audio/{audio_id} | Get audio track
[**instagram_get_comments**](InstagramApi.md#instagram_get_comments) | **GET** /v1/instagram/media/{code}/comments | Get comments
[**instagram_get_followers**](InstagramApi.md#instagram_get_followers) | **GET** /v1/instagram/users/{username}/followers | Get followers
[**instagram_get_following**](InstagramApi.md#instagram_get_following) | **GET** /v1/instagram/users/{username}/following | Get following
[**instagram_get_hashtag_info**](InstagramApi.md#instagram_get_hashtag_info) | **GET** /v1/instagram/hashtags/{tag} | Get hashtag info
[**instagram_get_highlights**](InstagramApi.md#instagram_get_highlights) | **GET** /v1/instagram/users/{username}/highlights | Get highlights
[**instagram_get_likers**](InstagramApi.md#instagram_get_likers) | **GET** /v1/instagram/media/{code}/likers | Get likers
[**instagram_get_location**](InstagramApi.md#instagram_get_location) | **GET** /v1/instagram/locations/{location_pk} | Get location
[**instagram_get_post_reel_detail**](InstagramApi.md#instagram_get_post_reel_detail) | **GET** /v1/instagram/media/{code} | Get post/reel detail
[**instagram_get_profile**](InstagramApi.md#instagram_get_profile) | **GET** /v1/instagram/users/{username} | Get profile
[**instagram_get_tagged_posts**](InstagramApi.md#instagram_get_tagged_posts) | **GET** /v1/instagram/users/{username}/tagged | Get tagged posts
[**instagram_get_user_posts**](InstagramApi.md#instagram_get_user_posts) | **GET** /v1/instagram/users/{username}/posts | Get user posts
[**instagram_get_user_reels**](InstagramApi.md#instagram_get_user_reels) | **GET** /v1/instagram/users/{username}/reels | Get user reels
[**instagram_health**](InstagramApi.md#instagram_health) | **GET** /v1/instagram/health | Health
[**instagram_health_head**](InstagramApi.md#instagram_health_head) | **HEAD** /v1/instagram/health | Health
[**instagram_recent_hashtag_posts**](InstagramApi.md#instagram_recent_hashtag_posts) | **GET** /v1/instagram/hashtags/{tag}/recent | Recent hashtag posts
[**instagram_related_profiles**](InstagramApi.md#instagram_related_profiles) | **GET** /v1/instagram/users/{username}/related | Related profiles
[**instagram_search_hashtags**](InstagramApi.md#instagram_search_hashtags) | **GET** /v1/instagram/search/hashtags | Search hashtags
[**instagram_search_users**](InstagramApi.md#instagram_search_users) | **GET** /v1/instagram/search/users | Search users
[**instagram_top_hashtag_posts**](InstagramApi.md#instagram_top_hashtag_posts) | **GET** /v1/instagram/hashtags/{tag}/top | Top hashtag posts



## instagram_about_this_account

> serde_json::Value instagram_about_this_account(username)
About this account

Country, join date and former usernames.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_blended_top_search

> serde_json::Value instagram_blended_top_search(query)
Blended top search

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_active_stories

> serde_json::Value instagram_get_active_stories(username)
Get active stories

Active stories (account pool only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_audio_track

> serde_json::Value instagram_get_audio_track(audio_id)
Get audio track

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audio_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_comments

> serde_json::Value instagram_get_comments(code, amount, cursor)
Get comments

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**code** | **String** |  | [required] |
**amount** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_followers

> serde_json::Value instagram_get_followers(username, amount, cursor, order)
Get followers

Followers list, paginated (account pool).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**amount** | Option<**i32**> |  |  |[default to 50]
**cursor** | Option<**String**> |  |  |
**order** | Option<**String**> | date_followed_latest | date_followed_earliest |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_following

> serde_json::Value instagram_get_following(username, amount, cursor)
Get following

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**amount** | Option<**i32**> |  |  |[default to 50]
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_hashtag_info

> serde_json::Value instagram_get_hashtag_info(tag)
Get hashtag info

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tag** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_highlights

> serde_json::Value instagram_get_highlights(username)
Get highlights

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_likers

> serde_json::Value instagram_get_likers(code)
Get likers

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**code** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_location

> serde_json::Value instagram_get_location(location_pk)
Get location

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**location_pk** | **i32** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_post_reel_detail

> serde_json::Value instagram_get_post_reel_detail(code)
Get post/reel detail

Single post or reel: caption, media, counts, tags, location, carousel.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**code** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_profile

> serde_json::Value instagram_get_profile(username)
Get profile

Full public profile: bio, counts, verification, business contact, links.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_tagged_posts

> serde_json::Value instagram_get_tagged_posts(username, amount, cursor)
Get tagged posts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**amount** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_user_posts

> serde_json::Value instagram_get_user_posts(username, amount, cursor)
Get user posts

Timeline posts, paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**amount** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_get_user_reels

> serde_json::Value instagram_get_user_reels(username, amount, cursor)
Get user reels

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**amount** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_health

> serde_json::Value instagram_health()
Health

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


## instagram_health_head

> serde_json::Value instagram_health_head()
Health

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


## instagram_recent_hashtag_posts

> serde_json::Value instagram_recent_hashtag_posts(tag, amount, cursor)
Recent hashtag posts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tag** | **String** |  | [required] |
**amount** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_related_profiles

> serde_json::Value instagram_related_profiles(username)
Related profiles

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_search_hashtags

> serde_json::Value instagram_search_hashtags(query)
Search hashtags

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_search_users

> serde_json::Value instagram_search_users(query)
Search users

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## instagram_top_hashtag_posts

> serde_json::Value instagram_top_hashtag_posts(tag, amount, cursor)
Top hashtag posts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tag** | **String** |  | [required] |
**amount** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

