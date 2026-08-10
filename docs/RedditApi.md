# \RedditApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**reddit_get_cross_posts**](RedditApi.md#reddit_get_cross_posts) | **GET** /v1/reddit/posts/{post_id}/duplicates | Get cross-posts
[**reddit_get_post_comments**](RedditApi.md#reddit_get_post_comments) | **GET** /v1/reddit/posts/{post_id}/comments | Get post comments
[**reddit_get_post_detail**](RedditApi.md#reddit_get_post_detail) | **GET** /v1/reddit/posts/{post_id} | Get post detail
[**reddit_get_posts_by_domain**](RedditApi.md#reddit_get_posts_by_domain) | **GET** /v1/reddit/domains/{domain}/posts | Get posts by domain
[**reddit_get_subreddit_info**](RedditApi.md#reddit_get_subreddit_info) | **GET** /v1/reddit/subreddits/{subreddit} | Get subreddit info
[**reddit_get_subreddit_posts**](RedditApi.md#reddit_get_subreddit_posts) | **GET** /v1/reddit/subreddits/{subreddit}/posts | Get subreddit posts
[**reddit_get_subreddit_rules**](RedditApi.md#reddit_get_subreddit_rules) | **GET** /v1/reddit/subreddits/{subreddit}/rules | Get subreddit rules
[**reddit_get_trending_posts**](RedditApi.md#reddit_get_trending_posts) | **GET** /v1/reddit/posts/trending | Get trending posts
[**reddit_get_user_profile**](RedditApi.md#reddit_get_user_profile) | **GET** /v1/reddit/users/{username} | Get user profile
[**reddit_get_user_s_comments**](RedditApi.md#reddit_get_user_s_comments) | **GET** /v1/reddit/users/{username}/comments | Get user's comments
[**reddit_get_user_s_moderated_subreddits**](RedditApi.md#reddit_get_user_s_moderated_subreddits) | **GET** /v1/reddit/users/{username}/moderated | Get user's moderated subreddits
[**reddit_get_user_s_posts**](RedditApi.md#reddit_get_user_s_posts) | **GET** /v1/reddit/users/{username}/posts | Get user's posts
[**reddit_get_user_s_trophies**](RedditApi.md#reddit_get_user_s_trophies) | **GET** /v1/reddit/users/{username}/trophies | Get user's trophies
[**reddit_get_wiki_page_content**](RedditApi.md#reddit_get_wiki_page_content) | **GET** /v1/reddit/subreddits/{subreddit}/wiki/{page} | Get wiki page content
[**reddit_list_wiki_pages**](RedditApi.md#reddit_list_wiki_pages) | **GET** /v1/reddit/subreddits/{subreddit}/wiki | List wiki pages
[**reddit_new_subreddits**](RedditApi.md#reddit_new_subreddits) | **GET** /v1/reddit/subreddits/new | New subreddits
[**reddit_popular_subreddits**](RedditApi.md#reddit_popular_subreddits) | **GET** /v1/reddit/subreddits/popular | Popular subreddits
[**reddit_reddit_scraper_health_check**](RedditApi.md#reddit_reddit_scraper_health_check) | **GET** /v1/reddit/health | Reddit scraper health check
[**reddit_reddit_scraper_health_check_head**](RedditApi.md#reddit_reddit_scraper_health_check_head) | **HEAD** /v1/reddit/health | Reddit scraper health check
[**reddit_search_reddit_posts**](RedditApi.md#reddit_search_reddit_posts) | **GET** /v1/reddit/search/posts | Search Reddit posts
[**reddit_search_subreddits**](RedditApi.md#reddit_search_subreddits) | **GET** /v1/reddit/search/subreddits | Search subreddits
[**reddit_search_users**](RedditApi.md#reddit_search_users) | **GET** /v1/reddit/search/users | Search users



## reddit_get_cross_posts

> serde_json::Value reddit_get_cross_posts(post_id, limit, after)
Get cross-posts

Get cross-posts and duplicates of a Reddit post.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_post_comments

> serde_json::Value reddit_get_post_comments(post_id, sort, limit, depth)
Get post comments

Get comment tree for a Reddit post.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**sort** | Option<**String**> | Sort: confidence, top, new, controversial, old, qa |  |[default to confidence]
**limit** | Option<**i32**> |  |  |[default to 25]
**depth** | Option<**i32**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_post_detail

> serde_json::Value reddit_get_post_detail(post_id)
Get post detail

Get detailed information about a Reddit post.

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


## reddit_get_posts_by_domain

> serde_json::Value reddit_get_posts_by_domain(domain, sort, t, limit, after)
Get posts by domain

Get Reddit posts linking to a specific domain.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**domain** | **String** |  | [required] |
**sort** | Option<**String**> |  |  |[default to hot]
**t** | Option<**String**> |  |  |[default to all]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_subreddit_info

> serde_json::Value reddit_get_subreddit_info(subreddit)
Get subreddit info

Get detailed information about a subreddit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**subreddit** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_subreddit_posts

> serde_json::Value reddit_get_subreddit_posts(subreddit, sort, t, limit, after)
Get subreddit posts

Get posts from a subreddit with sorting options.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**subreddit** | **String** |  | [required] |
**sort** | Option<**String**> | Sort: hot, new, top, rising, controversial |  |[default to hot]
**t** | Option<**String**> | Time filter |  |[default to all]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_subreddit_rules

> serde_json::Value reddit_get_subreddit_rules(subreddit)
Get subreddit rules

Get the rules of a subreddit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**subreddit** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_trending_posts

> serde_json::Value reddit_get_trending_posts(sort, t, limit, after)
Get trending posts

Get trending posts from Reddit's front page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sort** | Option<**String**> | Sort: hot, new, top, rising, controversial, best |  |[default to hot]
**t** | Option<**String**> | Time filter |  |[default to day]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_user_profile

> serde_json::Value reddit_get_user_profile(username)
Get user profile

Get a Reddit user's profile.

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


## reddit_get_user_s_comments

> serde_json::Value reddit_get_user_s_comments(username, sort, t, limit, after)
Get user's comments

Get comments by a Reddit user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**sort** | Option<**String**> |  |  |[default to new]
**t** | Option<**String**> |  |  |[default to all]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_user_s_moderated_subreddits

> serde_json::Value reddit_get_user_s_moderated_subreddits(username)
Get user's moderated subreddits

Get subreddits moderated by a user.

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


## reddit_get_user_s_posts

> serde_json::Value reddit_get_user_s_posts(username, sort, t, limit, after)
Get user's posts

Get posts submitted by a Reddit user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**sort** | Option<**String**> |  |  |[default to new]
**t** | Option<**String**> |  |  |[default to all]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_get_user_s_trophies

> serde_json::Value reddit_get_user_s_trophies(username)
Get user's trophies

Get a user's trophy case.

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


## reddit_get_wiki_page_content

> serde_json::Value reddit_get_wiki_page_content(subreddit, page)
Get wiki page content

Get the content of a specific wiki page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**subreddit** | **String** |  | [required] |
**page** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_list_wiki_pages

> serde_json::Value reddit_list_wiki_pages(subreddit)
List wiki pages

List all wiki pages in a subreddit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**subreddit** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_new_subreddits

> serde_json::Value reddit_new_subreddits(limit, after)
New subreddits

Get recently created subreddits.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_popular_subreddits

> serde_json::Value reddit_popular_subreddits(limit, after)
Popular subreddits

Get popular subreddits by subscriber count.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_reddit_scraper_health_check

> serde_json::Value reddit_reddit_scraper_health_check()
Reddit scraper health check

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


## reddit_reddit_scraper_health_check_head

> serde_json::Value reddit_reddit_scraper_health_check_head()
Reddit scraper health check

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


## reddit_search_reddit_posts

> serde_json::Value reddit_search_reddit_posts(q, subreddit, sort, t, limit, after)
Search Reddit posts

Search Reddit posts globally or within a subreddit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**subreddit** | Option<**String**> | Restrict to subreddit |  |
**sort** | Option<**String**> | Sort: relevance, hot, top, new, comments |  |[default to relevance]
**t** | Option<**String**> | Time: hour, day, week, month, year, all |  |[default to all]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_search_subreddits

> serde_json::Value reddit_search_subreddits(q, limit, after)
Search subreddits

Search for subreddits by keyword.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reddit_search_users

> serde_json::Value reddit_search_users(q, limit, after)
Search users

Search for Reddit users.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

