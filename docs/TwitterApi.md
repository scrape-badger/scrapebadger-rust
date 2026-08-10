# \TwitterApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**twitter_advanced_tweet_search**](TwitterApi.md#twitter_advanced_tweet_search) | **GET** /v1/twitter/tweets/advanced_search | Advanced tweet search
[**twitter_batch_get_users_by_ids**](TwitterApi.md#twitter_batch_get_users_by_ids) | **GET** /v1/twitter/users/batch_by_ids | Batch get users by IDs
[**twitter_batch_get_users_by_usernames**](TwitterApi.md#twitter_batch_get_users_by_usernames) | **GET** /v1/twitter/users/batch_by_usernames | Batch get users by usernames
[**twitter_configure_webhook_on_a_monitor**](TwitterApi.md#twitter_configure_webhook_on_a_monitor) | **POST** /v1/twitter/stream/webhooks | Configure webhook on a monitor
[**twitter_create_filter_rule**](TwitterApi.md#twitter_create_filter_rule) | **POST** /v1/twitter/stream/filter-rules | Create filter rule
[**twitter_create_stream_monitor**](TwitterApi.md#twitter_create_stream_monitor) | **POST** /v1/twitter/stream/monitors | Create stream monitor
[**twitter_delete_filter_rule**](TwitterApi.md#twitter_delete_filter_rule) | **DELETE** /v1/twitter/stream/filter-rules/{rule_id} | Delete filter rule
[**twitter_delete_stream_monitor**](TwitterApi.md#twitter_delete_stream_monitor) | **DELETE** /v1/twitter/stream/monitors/{monitor_id} | Delete stream monitor
[**twitter_get_article_by_id**](TwitterApi.md#twitter_get_article_by_id) | **GET** /v1/twitter/tweets/article/{article_id} | Get article by ID
[**twitter_get_broadcast_details**](TwitterApi.md#twitter_get_broadcast_details) | **GET** /v1/twitter/spaces/broadcast/{broadcast_id} | Get broadcast details
[**twitter_get_community_details**](TwitterApi.md#twitter_get_community_details) | **GET** /v1/twitter/communities/{community_id} | Get community details
[**twitter_get_community_notes**](TwitterApi.md#twitter_get_community_notes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/community_notes | Get community notes
[**twitter_get_community_tweets**](TwitterApi.md#twitter_get_community_tweets) | **GET** /v1/twitter/communities/{community_id}/tweets | Get community tweets
[**twitter_get_filter_rule**](TwitterApi.md#twitter_get_filter_rule) | **GET** /v1/twitter/stream/filter-rules/{rule_id} | Get filter rule
[**twitter_get_filter_rule_per_poll_rates**](TwitterApi.md#twitter_get_filter_rule_per_poll_rates) | **GET** /v1/twitter/stream/filter-rules-pricing | Get filter rule per-poll rates
[**twitter_get_list_details**](TwitterApi.md#twitter_get_list_details) | **GET** /v1/twitter/lists/{list_id}/detail | Get list details
[**twitter_get_list_tweets**](TwitterApi.md#twitter_get_list_tweets) | **GET** /v1/twitter/lists/{list_id}/tweets | Get list tweets
[**twitter_get_place_details**](TwitterApi.md#twitter_get_place_details) | **GET** /v1/twitter/geo/places/{place_id} | Get place details
[**twitter_get_similar_tweets**](TwitterApi.md#twitter_get_similar_tweets) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/similar | Get similar tweets
[**twitter_get_space_details**](TwitterApi.md#twitter_get_space_details) | **GET** /v1/twitter/spaces/{space_id} | Get Space details
[**twitter_get_stream_monitor**](TwitterApi.md#twitter_get_stream_monitor) | **GET** /v1/twitter/stream/monitors/{monitor_id} | Get stream monitor
[**twitter_get_trending_topics**](TwitterApi.md#twitter_get_trending_topics) | **GET** /v1/twitter/trends/ | Get trending topics
[**twitter_get_trends_by_location**](TwitterApi.md#twitter_get_trends_by_location) | **GET** /v1/twitter/trends/place/{woeid} | Get trends by location
[**twitter_get_tweet_details**](TwitterApi.md#twitter_get_tweet_details) | **GET** /v1/twitter/tweets/tweet/{tweet_id} | Get tweet details
[**twitter_get_tweet_edit_history**](TwitterApi.md#twitter_get_tweet_edit_history) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/edit_history | Get tweet edit history
[**twitter_get_tweet_favoriters**](TwitterApi.md#twitter_get_tweet_favoriters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/favoriters | Get tweet favoriters
[**twitter_get_tweet_quotes**](TwitterApi.md#twitter_get_tweet_quotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/quotes | Get tweet quotes
[**twitter_get_tweet_replies**](TwitterApi.md#twitter_get_tweet_replies) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/replies | Get tweet replies
[**twitter_get_tweet_retweeters**](TwitterApi.md#twitter_get_tweet_retweeters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/retweeters | Get tweet retweeters
[**twitter_get_tweets_by_ids**](TwitterApi.md#twitter_get_tweets_by_ids) | **GET** /v1/twitter/tweets/ | Get tweets by IDs
[**twitter_get_user_articles**](TwitterApi.md#twitter_get_user_articles) | **GET** /v1/twitter/users/{user_id}/articles | Get user articles
[**twitter_get_user_by_id**](TwitterApi.md#twitter_get_user_by_id) | **GET** /v1/twitter/users/{user_id}/by_id | Get user by ID
[**twitter_get_user_by_username**](TwitterApi.md#twitter_get_user_by_username) | **GET** /v1/twitter/users/{username}/by_username | Get user by username
[**twitter_get_user_followers**](TwitterApi.md#twitter_get_user_followers) | **GET** /v1/twitter/users/{username}/followers | Get user followers
[**twitter_get_user_following**](TwitterApi.md#twitter_get_user_following) | **GET** /v1/twitter/users/{username}/followings | Get user following
[**twitter_get_user_mentions**](TwitterApi.md#twitter_get_user_mentions) | **GET** /v1/twitter/users/{username}/mentions | Get user mentions
[**twitter_get_user_subscriptions**](TwitterApi.md#twitter_get_user_subscriptions) | **GET** /v1/twitter/users/{user_id}/subscriptions | Get user subscriptions
[**twitter_get_user_tweets**](TwitterApi.md#twitter_get_user_tweets) | **GET** /v1/twitter/users/{username}/latest_tweets | Get user tweets
[**twitter_list_billing_logs**](TwitterApi.md#twitter_list_billing_logs) | **GET** /v1/twitter/stream/billing-logs | List billing logs
[**twitter_list_delivery_logs_for_a_filter_rule**](TwitterApi.md#twitter_list_delivery_logs_for_a_filter_rule) | **GET** /v1/twitter/stream/filter-rules/{rule_id}/logs | List delivery logs for a filter rule
[**twitter_list_filter_rules**](TwitterApi.md#twitter_list_filter_rules) | **GET** /v1/twitter/stream/filter-rules | List filter rules
[**twitter_list_stream_monitors**](TwitterApi.md#twitter_list_stream_monitors) | **GET** /v1/twitter/stream/monitors | List stream monitors
[**twitter_list_tweet_delivery_logs**](TwitterApi.md#twitter_list_tweet_delivery_logs) | **GET** /v1/twitter/stream/logs | List tweet delivery logs
[**twitter_list_webhooks**](TwitterApi.md#twitter_list_webhooks) | **GET** /v1/twitter/stream/webhooks | List webhooks
[**twitter_remove_webhook_from_monitor**](TwitterApi.md#twitter_remove_webhook_from_monitor) | **DELETE** /v1/twitter/stream/webhooks/{webhook_id} | Remove webhook from monitor
[**twitter_search_communities**](TwitterApi.md#twitter_search_communities) | **GET** /v1/twitter/communities/search | Search communities
[**twitter_search_list_tweets**](TwitterApi.md#twitter_search_list_tweets) | **GET** /v1/twitter/lists/{list_id}/search_tweets | Search list tweets
[**twitter_search_places**](TwitterApi.md#twitter_search_places) | **GET** /v1/twitter/geo/search | Search places
[**twitter_search_users**](TwitterApi.md#twitter_search_users) | **GET** /v1/twitter/users/search_users | Search users
[**twitter_test_webhook_delivery**](TwitterApi.md#twitter_test_webhook_delivery) | **POST** /v1/twitter/stream/webhooks/test | Test webhook delivery
[**twitter_twitter_scraper_health_check**](TwitterApi.md#twitter_twitter_scraper_health_check) | **GET** /v1/twitter/health | Twitter scraper health check
[**twitter_twitter_scraper_health_check_head**](TwitterApi.md#twitter_twitter_scraper_health_check_head) | **HEAD** /v1/twitter/health | Twitter scraper health check
[**twitter_update_filter_rule**](TwitterApi.md#twitter_update_filter_rule) | **PATCH** /v1/twitter/stream/filter-rules/{rule_id} | Update filter rule
[**twitter_update_stream_monitor**](TwitterApi.md#twitter_update_stream_monitor) | **PATCH** /v1/twitter/stream/monitors/{monitor_id} | Update stream monitor
[**twitter_validate_search_query**](TwitterApi.md#twitter_validate_search_query) | **POST** /v1/twitter/stream/filter-rules/validate | Validate search query



## twitter_advanced_tweet_search

> serde_json::Value twitter_advanced_tweet_search(query, query_type, count, cursor)
Advanced tweet search

Search tweets with advanced options.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**query_type** | Option<**String**> |  |  |
**count** | Option<**i32**> |  |  |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_batch_get_users_by_ids

> serde_json::Value twitter_batch_get_users_by_ids(user_ids)
Batch get users by IDs

Get multiple user profiles by their numeric IDs (comma-separated).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_ids** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_batch_get_users_by_usernames

> serde_json::Value twitter_batch_get_users_by_usernames(usernames)
Batch get users by usernames

Get multiple user profiles by their usernames (comma-separated).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**usernames** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_configure_webhook_on_a_monitor

> models::WebhookResponse twitter_configure_webhook_on_a_monitor(webhook_create)
Configure webhook on a monitor

Configure a webhook delivery URL on a stream monitor.  The secret is returned only once on creation. Subsequent calls show secret_set: bool. If monitor already has a webhook, delete it first (409 is returned).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_create** | [**WebhookCreate**](WebhookCreate.md) |  | [required] |

### Return type

[**models::WebhookResponse**](WebhookResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_create_filter_rule

> models::FilterRuleResponse twitter_create_filter_rule(filter_rule_create)
Create filter rule

Create a new query-based tweet filter rule.  The rule starts in 'active' status immediately. Credits must be positive. The (api_key_id, tag) pair must be unique.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**filter_rule_create** | [**FilterRuleCreate**](FilterRuleCreate.md) |  | [required] |

### Return type

[**models::FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_create_stream_monitor

> models::StreamMonitorResponse twitter_create_stream_monitor(stream_monitor_create)
Create stream monitor

Create a new stream monitor to watch Twitter accounts in real-time.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**stream_monitor_create** | [**StreamMonitorCreate**](StreamMonitorCreate.md) |  | [required] |

### Return type

[**models::StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_delete_filter_rule

> twitter_delete_filter_rule(rule_id)
Delete filter rule

Delete a filter rule and all its logs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_delete_stream_monitor

> twitter_delete_stream_monitor(monitor_id)
Delete stream monitor

Delete a stream monitor and all its logs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**monitor_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_article_by_id

> serde_json::Value twitter_get_article_by_id(article_id)
Get article by ID

Get a long-form article by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**article_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_broadcast_details

> serde_json::Value twitter_get_broadcast_details(broadcast_id)
Get broadcast details

Get details of a live video broadcast.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**broadcast_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_community_details

> serde_json::Value twitter_get_community_details(community_id)
Get community details

Get details of a specific community.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**community_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_community_notes

> serde_json::Value twitter_get_community_notes(tweet_id)
Get community notes

Get community notes (Birdwatch) for a specific tweet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweet_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_community_tweets

> serde_json::Value twitter_get_community_tweets(community_id, tweet_type, cursor)
Get community tweets

Get tweets from a specific community.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**community_id** | **String** |  | [required] |
**tweet_type** | Option<**String**> |  |  |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_filter_rule

> models::FilterRuleResponse twitter_get_filter_rule(rule_id)
Get filter rule

Get a single filter rule by ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |

### Return type

[**models::FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_filter_rule_per_poll_rates

> models::PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse twitter_get_filter_rule_per_poll_rates()
Get filter rule per-poll rates

Current per-poll rates (auth required — used by SDK + dashboard).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse**](portal_api__routers__v1_twitter_filter_rules__FilterRulePricingResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_list_details

> serde_json::Value twitter_get_list_details(list_id)
Get list details

Get details of a specific list.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_list_tweets

> serde_json::Value twitter_get_list_tweets(list_id, cursor)
Get list tweets

Get tweets from a specific list.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_place_details

> serde_json::Value twitter_get_place_details(place_id)
Get place details

Get details of a specific place.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**place_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_similar_tweets

> serde_json::Value twitter_get_similar_tweets(tweet_id)
Get similar tweets

Get tweets similar to a specific tweet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweet_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_space_details

> serde_json::Value twitter_get_space_details(space_id)
Get Space details

Get details of a Twitter Space.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**space_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_stream_monitor

> models::StreamMonitorResponse twitter_get_stream_monitor(monitor_id)
Get stream monitor

Get a single stream monitor by ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**monitor_id** | **String** |  | [required] |

### Return type

[**models::StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_trending_topics

> serde_json::Value twitter_get_trending_topics(category, count)
Get trending topics

Get trending topics.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category** | Option<**String**> |  |  |
**count** | Option<**i32**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_trends_by_location

> serde_json::Value twitter_get_trends_by_location(woeid)
Get trends by location

Get trending topics for a specific location (WOEID).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**woeid** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_tweet_details

> serde_json::Value twitter_get_tweet_details(tweet_id, cursor)
Get tweet details

Get detailed information about a specific tweet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweet_id** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_tweet_edit_history

> serde_json::Value twitter_get_tweet_edit_history(tweet_id)
Get tweet edit history

Get the edit history of a tweet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweet_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_tweet_favoriters

> serde_json::Value twitter_get_tweet_favoriters(tweet_id, cursor)
Get tweet favoriters

Get users who favorited a specific tweet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweet_id** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_tweet_quotes

> serde_json::Value twitter_get_tweet_quotes(tweet_id, cursor)
Get tweet quotes

Get tweets that quote a specific tweet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweet_id** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_tweet_replies

> serde_json::Value twitter_get_tweet_replies(tweet_id, cursor)
Get tweet replies

Get replies to a specific tweet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweet_id** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_tweet_retweeters

> serde_json::Value twitter_get_tweet_retweeters(tweet_id, cursor)
Get tweet retweeters

Get users who retweeted a specific tweet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweet_id** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_tweets_by_ids

> serde_json::Value twitter_get_tweets_by_ids(tweets)
Get tweets by IDs

Get multiple tweets by their IDs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**tweets** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_user_articles

> serde_json::Value twitter_get_user_articles(user_id, cursor)
Get user articles

Get long-form articles written by a user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_user_by_id

> serde_json::Value twitter_get_user_by_id(user_id)
Get user by ID

Get user profile by user ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_user_by_username

> serde_json::Value twitter_get_user_by_username(username)
Get user by username

Get user profile by username.

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


## twitter_get_user_followers

> serde_json::Value twitter_get_user_followers(username, cursor)
Get user followers

Get followers of a specific user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_user_following

> serde_json::Value twitter_get_user_following(username, cursor)
Get user following

Get users that a specific user is following.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_user_mentions

> serde_json::Value twitter_get_user_mentions(username, count, cursor)
Get user mentions

Get tweets mentioning a specific user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**count** | Option<**i32**> |  |  |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_user_subscriptions

> serde_json::Value twitter_get_user_subscriptions(user_id, cursor)
Get user subscriptions

Get subscriptions of a specific user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_get_user_tweets

> serde_json::Value twitter_get_user_tweets(username, cursor)
Get user tweets

Get latest tweets from a specific user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_list_billing_logs

> models::BillingLogListResponse twitter_list_billing_logs(monitor_id, page, page_size)
List billing logs

List billing activity logs for the authenticated API key's monitors.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**monitor_id** | Option<**String**> |  |  |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 20]

### Return type

[**models::BillingLogListResponse**](BillingLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_list_delivery_logs_for_a_filter_rule

> models::FilterRuleDeliveryLogListResponse twitter_list_delivery_logs_for_a_filter_rule(rule_id, delivery_status, author_username, page, page_size, sort)
List delivery logs for a filter rule

List tweet delivery logs for a specific filter rule.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |
**delivery_status** | Option<**String**> |  |  |
**author_username** | Option<**String**> |  |  |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 20]
**sort** | Option<**String**> |  |  |[default to desc]

### Return type

[**models::FilterRuleDeliveryLogListResponse**](FilterRuleDeliveryLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_list_filter_rules

> models::FilterRuleListResponse twitter_list_filter_rules(status, page, page_size)
List filter rules

List all filter rules for the authenticated API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> |  |  |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 20]

### Return type

[**models::FilterRuleListResponse**](FilterRuleListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_list_stream_monitors

> models::StreamMonitorListResponse twitter_list_stream_monitors(status, page, page_size)
List stream monitors

List all stream monitors for the authenticated API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> |  |  |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 20]

### Return type

[**models::StreamMonitorListResponse**](StreamMonitorListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_list_tweet_delivery_logs

> models::TweetDeliveryLogListResponse twitter_list_tweet_delivery_logs(monitor_id, author_username, delivery_status, page, page_size, sort)
List tweet delivery logs

List tweet delivery logs for the authenticated API key's monitors.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**monitor_id** | Option<**String**> |  |  |
**author_username** | Option<**String**> |  |  |
**delivery_status** | Option<**String**> |  |  |
**page** | Option<**i32**> |  |  |[default to 1]
**page_size** | Option<**i32**> |  |  |[default to 20]
**sort** | Option<**String**> |  |  |[default to desc]

### Return type

[**models::TweetDeliveryLogListResponse**](TweetDeliveryLogListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_list_webhooks

> models::WebhookListResponse twitter_list_webhooks(monitor_id)
List webhooks

List all webhook-configured monitors for the authenticated API key.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**monitor_id** | Option<**String**> |  |  |

### Return type

[**models::WebhookListResponse**](WebhookListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_remove_webhook_from_monitor

> twitter_remove_webhook_from_monitor(webhook_id)
Remove webhook from monitor

Remove webhook configuration from a monitor. webhook_id is the monitor_id.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_search_communities

> serde_json::Value twitter_search_communities(query, cursor)
Search communities

Search for communities by query.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_search_list_tweets

> serde_json::Value twitter_search_list_tweets(list_id, query, cursor)
Search list tweets

Search tweets within a specific list.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **String** |  | [required] |
**query** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_search_places

> serde_json::Value twitter_search_places(query, lat, long)
Search places

Search for places by query or coordinates.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | Option<**String**> |  |  |
**lat** | Option<**f64**> |  |  |
**long** | Option<**f64**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_search_users

> serde_json::Value twitter_search_users(query, cursor)
Search users

Search for users by query.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**cursor** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_test_webhook_delivery

> models::WebhookTestResponse twitter_test_webhook_delivery(webhook_test_request)
Test webhook delivery

Send a test payload to a monitor's webhook URL.  The test payload has type=\"test\" instead of type=\"tweet\". Makes a synchronous HTTP POST and returns the delivery result.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_test_request** | [**WebhookTestRequest**](WebhookTestRequest.md) |  | [required] |

### Return type

[**models::WebhookTestResponse**](WebhookTestResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_twitter_scraper_health_check

> serde_json::Value twitter_twitter_scraper_health_check()
Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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


## twitter_twitter_scraper_health_check_head

> serde_json::Value twitter_twitter_scraper_health_check_head()
Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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


## twitter_update_filter_rule

> models::FilterRuleResponse twitter_update_filter_rule(rule_id, filter_rule_update)
Update filter rule

Partially update a filter rule.  Setting status='active' on a paused rule performs a credit check.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |
**filter_rule_update** | [**FilterRuleUpdate**](FilterRuleUpdate.md) |  | [required] |

### Return type

[**models::FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_update_stream_monitor

> models::StreamMonitorResponse twitter_update_stream_monitor(monitor_id, stream_monitor_update)
Update stream monitor

Partially update a stream monitor.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**monitor_id** | **String** |  | [required] |
**stream_monitor_update** | [**StreamMonitorUpdate**](StreamMonitorUpdate.md) |  | [required] |

### Return type

[**models::StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## twitter_validate_search_query

> models::FilterRuleValidateResponse twitter_validate_search_query(filter_rule_validate_request)
Validate search query

Validate a Twitter search query string.  Performs basic structural validation without making a live Twitter request. Returns valid=True if the query passes syntax checks.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**filter_rule_validate_request** | [**FilterRuleValidateRequest**](FilterRuleValidateRequest.md) |  | [required] |

### Return type

[**models::FilterRuleValidateResponse**](FilterRuleValidateResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

