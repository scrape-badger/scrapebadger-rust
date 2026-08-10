# \YouTubeApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**youtube_batch_video_detail**](YouTubeApi.md#youtube_batch_video_detail) | **POST** /v1/youtube/videos/batch | Batch video detail
[**youtube_channel_about**](YouTubeApi.md#youtube_channel_about) | **GET** /v1/youtube/channels/{channel_id}/about | Channel about
[**youtube_channel_playlists**](YouTubeApi.md#youtube_channel_playlists) | **GET** /v1/youtube/channels/{channel_id}/playlists | Channel playlists
[**youtube_channel_shorts**](YouTubeApi.md#youtube_channel_shorts) | **GET** /v1/youtube/channels/{channel_id}/shorts | Channel shorts
[**youtube_channel_streams**](YouTubeApi.md#youtube_channel_streams) | **GET** /v1/youtube/channels/{channel_id}/streams | Channel streams
[**youtube_channel_videos**](YouTubeApi.md#youtube_channel_videos) | **GET** /v1/youtube/channels/{channel_id}/videos | Channel videos
[**youtube_comment_replies**](YouTubeApi.md#youtube_comment_replies) | **GET** /v1/youtube/videos/{video_id}/comments/{comment_id}/replies | Comment replies
[**youtube_community_post_comments**](YouTubeApi.md#youtube_community_post_comments) | **GET** /v1/youtube/posts/{post_id}/comments | Community post comments
[**youtube_community_posts**](YouTubeApi.md#youtube_community_posts) | **GET** /v1/youtube/channels/{channel_id}/community | Community posts
[**youtube_content_regions**](YouTubeApi.md#youtube_content_regions) | **GET** /v1/youtube/regions | Content regions
[**youtube_get_a_community_post**](YouTubeApi.md#youtube_get_a_community_post) | **GET** /v1/youtube/posts/{post_id} | Get a community post
[**youtube_get_a_mix_radio_queue**](YouTubeApi.md#youtube_get_a_mix_radio_queue) | **GET** /v1/youtube/mixes/{playlist_id} | Get a mix / radio queue
[**youtube_get_a_short**](YouTubeApi.md#youtube_get_a_short) | **GET** /v1/youtube/shorts/{video_id} | Get a Short
[**youtube_get_channel_detail**](YouTubeApi.md#youtube_get_channel_detail) | **GET** /v1/youtube/channels/{channel_id} | Get channel detail
[**youtube_get_playlist_detail**](YouTubeApi.md#youtube_get_playlist_detail) | **GET** /v1/youtube/playlists/{playlist_id} | Get playlist detail
[**youtube_get_video_detail**](YouTubeApi.md#youtube_get_video_detail) | **GET** /v1/youtube/videos/{video_id} | Get video detail
[**youtube_guest_home_feed**](YouTubeApi.md#youtube_guest_home_feed) | **GET** /v1/youtube/home | Guest home feed
[**youtube_keyword_suggestions**](YouTubeApi.md#youtube_keyword_suggestions) | **GET** /v1/youtube/autocomplete | Keyword suggestions
[**youtube_list_caption_tracks**](YouTubeApi.md#youtube_list_caption_tracks) | **GET** /v1/youtube/videos/{video_id}/captions | List caption tracks
[**youtube_live_chat_messages**](YouTubeApi.md#youtube_live_chat_messages) | **GET** /v1/youtube/videos/{video_id}/live_chat | Live chat messages
[**youtube_oembed_metadata**](YouTubeApi.md#youtube_oembed_metadata) | **GET** /v1/youtube/oembed | oEmbed metadata
[**youtube_playlist_items_page**](YouTubeApi.md#youtube_playlist_items_page) | **GET** /v1/youtube/playlists/{playlist_id}/items | Playlist items page
[**youtube_related_videos**](YouTubeApi.md#youtube_related_videos) | **GET** /v1/youtube/videos/{video_id}/related | Related videos
[**youtube_resolve_handle_url_to_id**](YouTubeApi.md#youtube_resolve_handle_url_to_id) | **GET** /v1/youtube/channels/resolve | Resolve handle/URL to id
[**youtube_search_within_a_channel**](YouTubeApi.md#youtube_search_within_a_channel) | **GET** /v1/youtube/channels/{channel_id}/search | Search within a channel
[**youtube_search_youtube**](YouTubeApi.md#youtube_search_youtube) | **GET** /v1/youtube/search | Search YouTube
[**youtube_search_youtube_music**](YouTubeApi.md#youtube_search_youtube_music) | **GET** /v1/youtube/music/search | Search YouTube Music
[**youtube_shorts_by_sound**](YouTubeApi.md#youtube_shorts_by_sound) | **GET** /v1/youtube/shorts/by_sound/{sound_id} | Shorts by sound
[**youtube_stream_formats**](YouTubeApi.md#youtube_stream_formats) | **GET** /v1/youtube/videos/{video_id}/streams | Stream formats
[**youtube_subscriber_count_fast**](YouTubeApi.md#youtube_subscriber_count_fast) | **GET** /v1/youtube/channels/{channel_id}/subscriber_count | Subscriber count (fast)
[**youtube_supported_markets**](YouTubeApi.md#youtube_supported_markets) | **GET** /v1/youtube/markets | Supported markets
[**youtube_trending_shorts**](YouTubeApi.md#youtube_trending_shorts) | **GET** /v1/youtube/trending/shorts | Trending shorts
[**youtube_trending_videos**](YouTubeApi.md#youtube_trending_videos) | **GET** /v1/youtube/trending | Trending videos
[**youtube_ui_languages**](YouTubeApi.md#youtube_ui_languages) | **GET** /v1/youtube/languages | UI languages
[**youtube_video_categories**](YouTubeApi.md#youtube_video_categories) | **GET** /v1/youtube/categories | Video categories
[**youtube_video_comments**](YouTubeApi.md#youtube_video_comments) | **GET** /v1/youtube/videos/{video_id}/comments | Video comments
[**youtube_video_transcript**](YouTubeApi.md#youtube_video_transcript) | **GET** /v1/youtube/videos/{video_id}/transcript | Video transcript
[**youtube_videos_under_a_hashtag**](YouTubeApi.md#youtube_videos_under_a_hashtag) | **GET** /v1/youtube/hashtags/{tag} | Videos under a hashtag
[**youtube_youtube_scraper_health_check**](YouTubeApi.md#youtube_youtube_scraper_health_check) | **GET** /v1/youtube/health | YouTube scraper health check
[**youtube_youtube_scraper_health_check_head**](YouTubeApi.md#youtube_youtube_scraper_health_check_head) | **HEAD** /v1/youtube/health | YouTube scraper health check



## youtube_batch_video_detail

> serde_json::Value youtube_batch_video_detail(request_body)
Batch video detail

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md) |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_channel_about

> serde_json::Value youtube_channel_about(channel_id)
Channel about

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_channel_playlists

> serde_json::Value youtube_channel_playlists(channel_id)
Channel playlists

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_channel_shorts

> serde_json::Value youtube_channel_shorts(channel_id)
Channel shorts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_channel_streams

> serde_json::Value youtube_channel_streams(channel_id)
Channel streams

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_channel_videos

> serde_json::Value youtube_channel_videos(channel_id)
Channel videos

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_comment_replies

> serde_json::Value youtube_comment_replies(video_id, comment_id, continuation)
Comment replies

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**continuation** | **String** | Replies continuation token | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_community_post_comments

> serde_json::Value youtube_community_post_comments(post_id)
Community post comments

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


## youtube_community_posts

> serde_json::Value youtube_community_posts(channel_id)
Community posts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_content_regions

> serde_json::Value youtube_content_regions()
Content regions

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


## youtube_get_a_community_post

> serde_json::Value youtube_get_a_community_post(post_id)
Get a community post

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


## youtube_get_a_mix_radio_queue

> serde_json::Value youtube_get_a_mix_radio_queue(playlist_id)
Get a mix / radio queue

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**playlist_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_get_a_short

> serde_json::Value youtube_get_a_short(video_id)
Get a Short

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_get_channel_detail

> serde_json::Value youtube_get_channel_detail(channel_id, gl, hl)
Get channel detail

Channel detail (accepts a UC id, @handle, or custom URL).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |
**gl** | Option<**String**> |  |  |
**hl** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_get_playlist_detail

> serde_json::Value youtube_get_playlist_detail(playlist_id)
Get playlist detail

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**playlist_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_get_video_detail

> serde_json::Value youtube_get_video_detail(video_id, gl, hl)
Get video detail

Full video detail — merged player + next (likes, comments, chapters, related).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**gl** | Option<**String**> |  |  |
**hl** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_guest_home_feed

> serde_json::Value youtube_guest_home_feed()
Guest home feed

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


## youtube_keyword_suggestions

> serde_json::Value youtube_keyword_suggestions(query, gl, hl)
Keyword suggestions

Return YouTube keyword autocomplete suggestions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Partial query prefix | [required] |
**gl** | Option<**String**> |  |  |
**hl** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_list_caption_tracks

> serde_json::Value youtube_list_caption_tracks(video_id)
List caption tracks

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_live_chat_messages

> serde_json::Value youtube_live_chat_messages(video_id, continuation, replay)
Live chat messages

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**continuation** | Option<**String**> |  |  |
**replay** | Option<**bool**> |  |  |[default to false]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_oembed_metadata

> serde_json::Value youtube_oembed_metadata(url)
oEmbed metadata

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | A YouTube URL | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_playlist_items_page

> serde_json::Value youtube_playlist_items_page(playlist_id)
Playlist items page

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**playlist_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_related_videos

> serde_json::Value youtube_related_videos(video_id)
Related videos

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_resolve_handle_url_to_id

> serde_json::Value youtube_resolve_handle_url_to_id(handle, url)
Resolve handle/URL to id

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**handle** | Option<**String**> |  |  |
**url** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_search_within_a_channel

> serde_json::Value youtube_search_within_a_channel(channel_id, query)
Search within a channel

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |
**query** | **String** | Search keywords | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_search_youtube

> serde_json::Value youtube_search_youtube(query, r#type, sort_by, upload_date, duration, features, gl, hl, continuation)
Search YouTube

Search videos / channels / playlists with the full filter matrix.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords | [required] |
**r#type** | Option<**String**> | video|channel|playlist|movie|all |  |
**sort_by** | Option<**String**> | relevance|date|views|rating |  |
**upload_date** | Option<**String**> | hour|today|week|month|year |  |
**duration** | Option<**String**> | short|medium|long |  |
**features** | Option<**String**> | hd,4k,360,vr180,3d,hdr,cc,subtitles,live |  |
**gl** | Option<**String**> | Content region (US, GB, DE…) |  |
**hl** | Option<**String**> | UI language |  |
**continuation** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_search_youtube_music

> serde_json::Value youtube_search_youtube_music(query)
Search YouTube Music

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Search keywords | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_shorts_by_sound

> serde_json::Value youtube_shorts_by_sound(sound_id)
Shorts by sound

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sound_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_stream_formats

> serde_json::Value youtube_stream_formats(video_id, client)
Stream formats

Stream/format metadata (best-effort; media URLs may be PO-token gated).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**client** | Option<**String**> | IOS|ANDROID|WEB |  |[default to IOS]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_subscriber_count_fast

> serde_json::Value youtube_subscriber_count_fast(channel_id)
Subscriber count (fast)

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_supported_markets

> serde_json::Value youtube_supported_markets()
Supported markets

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


## youtube_trending_shorts

> serde_json::Value youtube_trending_shorts()
Trending shorts

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


## youtube_trending_videos

> serde_json::Value youtube_trending_videos(gl, r#type)
Trending videos

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**gl** | Option<**String**> |  |  |
**r#type** | Option<**String**> | now|music|gaming|movies |  |[default to now]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_ui_languages

> serde_json::Value youtube_ui_languages()
UI languages

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


## youtube_video_categories

> serde_json::Value youtube_video_categories(gl)
Video categories

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**gl** | Option<**String**> |  |  |[default to US]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_video_comments

> serde_json::Value youtube_video_comments(video_id, sort_by, continuation)
Video comments

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**sort_by** | Option<**String**> | top|newest |  |[default to top]
**continuation** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_video_transcript

> serde_json::Value youtube_video_transcript(video_id, language)
Video transcript

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** |  | [required] |
**language** | Option<**String**> | BCP-47 language code |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## youtube_videos_under_a_hashtag

> serde_json::Value youtube_videos_under_a_hashtag(tag)
Videos under a hashtag

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


## youtube_youtube_scraper_health_check

> serde_json::Value youtube_youtube_scraper_health_check()
YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

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


## youtube_youtube_scraper_health_check_head

> serde_json::Value youtube_youtube_scraper_health_check_head()
YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

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

