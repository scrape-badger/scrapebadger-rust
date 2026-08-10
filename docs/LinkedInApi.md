# \LinkedInApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**linkedin_get_a_company_s_job_postings**](LinkedInApi.md#linkedin_get_a_company_s_job_postings) | **GET** /v1/linkedin/companies/{company_id}/jobs | Get a company's job postings
[**linkedin_get_a_course**](LinkedInApi.md#linkedin_get_a_course) | **GET** /v1/linkedin/learning/{course_slug} | Get a course
[**linkedin_get_a_public_article**](LinkedInApi.md#linkedin_get_a_public_article) | **GET** /v1/linkedin/articles/{article_slug} | Get a public article
[**linkedin_get_a_public_post**](LinkedInApi.md#linkedin_get_a_public_post) | **GET** /v1/linkedin/posts/{post_slug} | Get a public post
[**linkedin_get_company**](LinkedInApi.md#linkedin_get_company) | **GET** /v1/linkedin/companies/{universal_name} | Get company
[**linkedin_get_job_detail**](LinkedInApi.md#linkedin_get_job_detail) | **GET** /v1/linkedin/jobs/{job_id} | Get job detail
[**linkedin_get_public_profile**](LinkedInApi.md#linkedin_get_public_profile) | **GET** /v1/linkedin/profiles/{public_id} | Get public profile
[**linkedin_get_school**](LinkedInApi.md#linkedin_get_school) | **GET** /v1/linkedin/schools/{universal_name} | Get school
[**linkedin_linkedin_scraper_health_check**](LinkedInApi.md#linkedin_linkedin_scraper_health_check) | **GET** /v1/linkedin/health | LinkedIn scraper health check
[**linkedin_linkedin_scraper_health_check_head**](LinkedInApi.md#linkedin_linkedin_scraper_health_check_head) | **HEAD** /v1/linkedin/health | LinkedIn scraper health check
[**linkedin_search_linkedin_jobs**](LinkedInApi.md#linkedin_search_linkedin_jobs) | **GET** /v1/linkedin/jobs/search | Search LinkedIn jobs
[**linkedin_suggest_location_geo_ids**](LinkedInApi.md#linkedin_suggest_location_geo_ids) | **GET** /v1/linkedin/geo/suggest | Suggest location geo ids



## linkedin_get_a_company_s_job_postings

> serde_json::Value linkedin_get_a_company_s_job_postings(company_id, start, country)
Get a company's job postings

Public job postings for a company (numeric company id from the company endpoint).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**company_id** | **String** |  | [required] |
**start** | Option<**i32**> | Pagination offset (0, 25, 50, ...) |  |[default to 0]
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_get_a_course

> serde_json::Value linkedin_get_a_course(course_slug, country)
Get a course

A public LinkedIn Learning course — provider, workload, instructors, rating.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**course_slug** | **String** |  | [required] |
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_get_a_public_article

> serde_json::Value linkedin_get_a_public_article(article_slug, country)
Get a public article

A public Pulse article — title, body, author, reactions (JSON-LD).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**article_slug** | **String** |  | [required] |
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_get_a_public_post

> serde_json::Value linkedin_get_a_public_post(post_slug, country)
Get a public post

A public activity share — text, author, reactions, comments (JSON-LD).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_slug** | **String** |  | [required] |
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_get_company

> serde_json::Value linkedin_get_company(universal_name, country)
Get company

Public company page — industry, size, HQ, followers, specialties (JSON-LD + SSR).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**universal_name** | **String** |  | [required] |
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_get_job_detail

> serde_json::Value linkedin_get_job_detail(job_id, country)
Get job detail

Full detail for one job posting (guest API, no login).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**job_id** | **String** |  | [required] |
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_get_public_profile

> serde_json::Value linkedin_get_public_profile(public_id, country)
Get public profile

Public profile by vanity id (the ``/in/{public_id}`` slug) — name, headline, location, about, experience, education (public JSON-LD + SSR subset).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**public_id** | **String** |  | [required] |
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_get_school

> serde_json::Value linkedin_get_school(universal_name, country)
Get school

Public school page — name, description, website, follower/alumni counts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**universal_name** | **String** |  | [required] |
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_linkedin_scraper_health_check

> serde_json::Value linkedin_linkedin_scraper_health_check()
LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

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


## linkedin_linkedin_scraper_health_check_head

> serde_json::Value linkedin_linkedin_scraper_health_check_head()
LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

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


## linkedin_search_linkedin_jobs

> serde_json::Value linkedin_search_linkedin_jobs(keywords, location, geo_id, company_id, date_posted, experience, job_type, workplace, sort, start, country)
Search LinkedIn jobs

Search public LinkedIn job postings (guest API, no login).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**keywords** | Option<**String**> | Job title / keywords |  |
**location** | Option<**String**> | Location text, e.g. 'New York' |  |
**geo_id** | Option<**String**> | LinkedIn numeric geo id (overrides location) |  |
**company_id** | Option<**String**> | Restrict to a company (numeric id) |  |
**date_posted** | Option<**String**> | past_24h | past_week | past_month | any |  |
**experience** | Option<**String**> | internship|entry|associate|mid_senior|director|executive (comma-separated) |  |
**job_type** | Option<**String**> | full_time|part_time|contract|temporary|internship|volunteer|other |  |
**workplace** | Option<**String**> | onsite|remote|hybrid (comma-separated) |  |
**sort** | Option<**String**> | relevant | recent |  |
**start** | Option<**i32**> | Pagination offset (0, 25, 50, ...) |  |[default to 0]
**country** | Option<**String**> | Residential proxy country |  |[default to us]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## linkedin_suggest_location_geo_ids

> serde_json::Value linkedin_suggest_location_geo_ids(query, r#type)
Suggest location geo ids

Resolve a name to LinkedIn ids (job-search ``geo_id`` / ``company_id`` helper).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Location text, e.g. 'London' | [required] |
**r#type** | Option<**String**> | geo | company |  |[default to geo]

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

