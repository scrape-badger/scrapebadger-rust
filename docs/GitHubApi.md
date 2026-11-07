# \GitHubApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**github_get_profile**](GitHubApi.md#github_get_profile) | **GET** /v1/github/profiles/{username} | Get profile



## github_get_profile

> models::GitHubProfileResponse github_get_profile(username, tab, year, page, next_page_token)
Get profile

Public user or organization profile, pins/popular repositories, README and contributions.  The overview preserves GitHub's public website sections, including organization-specific metadata. Compact displayed counts are approximate and marked with *_approximate. Unavailable or blocked data is an unbilled error, never an empty success.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**username** | **String** |  | [required] |
**tab** | Option<**String**> | Profile section; stars is available for users only |  |[default to overview]
**year** | Option<**i32**> | Overview only: 1970 through the current UTC year; activity is December or current month |  |
**page** | Option<**i32**> | Repositories only: page number, 30 rows per page |  |
**next_page_token** | Option<**String**> | Stars only: previous pagination.next_page_token |  |

### Return type

[**models::GitHubProfileResponse**](GitHubProfileResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

