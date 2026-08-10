# \WebApi

All URIs are relative to *https://scrapebadger.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**web_detect_anti_bot_and_captcha_systems**](WebApi.md#web_detect_anti_bot_and_captcha_systems) | **POST** /v1/web/detect | Detect anti-bot and CAPTCHA systems
[**web_extract_structured_data**](WebApi.md#web_extract_structured_data) | **POST** /v1/web/extract | Extract structured data
[**web_get_batch_job_status**](WebApi.md#web_get_batch_job_status) | **GET** /v1/web/batch/{job_id} | Get batch job status
[**web_poll_an_auto_unblock_discovery_job**](WebApi.md#web_poll_an_auto_unblock_discovery_job) | **GET** /v1/web/unblock/{job_id} | Poll an auto-unblock discovery job
[**web_scrape_a_url**](WebApi.md#web_scrape_a_url) | **POST** /v1/web/scrape | Scrape a URL
[**web_submit_batch_scraping_job**](WebApi.md#web_submit_batch_scraping_job) | **POST** /v1/web/batch | Submit batch scraping job
[**web_take_a_screenshot**](WebApi.md#web_take_a_screenshot) | **POST** /v1/web/screenshot | Take a screenshot
[**web_web_scraper_health_check**](WebApi.md#web_web_scraper_health_check) | **GET** /v1/web/health | Web scraper health check
[**web_web_scraper_health_check_head**](WebApi.md#web_web_scraper_health_check_head) | **HEAD** /v1/web/health | Web scraper health check



## web_detect_anti_bot_and_captcha_systems

> serde_json::Value web_detect_anti_bot_and_captcha_systems()
Detect anti-bot and CAPTCHA systems

Detect which anti-bot and CAPTCHA systems are present on a URL.  Uses rnet to fetch the page and identify DataDome, Cloudflare, Akamai, Kasada, Amazon WAF, reCAPTCHA, hCaptcha, GeeTest, and more. Cost: 1 credit.

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


## web_extract_structured_data

> serde_json::Value web_extract_structured_data()
Extract structured data

Extract structured data from a URL using CSS or XPath selectors. (Phase 6)

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


## web_get_batch_job_status

> serde_json::Value web_get_batch_job_status(job_id)
Get batch job status

Get the status of a batch scraping job. (Phase 6)

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**job_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## web_poll_an_auto_unblock_discovery_job

> serde_json::Value web_poll_an_auto_unblock_discovery_job(job_id)
Poll an auto-unblock discovery job

Return the status + progress narration for an auto-unblock job.  Polled by the playground loader. ``job_id`` is an unguessable UUID handed out in the ``202 unblocking`` envelope and acts as a capability token, so any authenticated caller holding it can read the job (this is what lets several users share one discovery run's loader).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**job_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## web_scrape_a_url

> serde_json::Value web_scrape_a_url()
Scrape a URL

Scrape a URL and return its content.  The Generic Web Scraping API is fully user-driven: callers pick their own request parameters (engine, proxy tier, country, JS rendering, …). A blocked target surfaces the raw 422 ``blocking_page_detected`` so the caller can tune parameters themselves — we do NOT auto-trigger host discovery. Curated per-origin overrides (which the dedicated scraper APIs depend on) still apply.

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


## web_submit_batch_scraping_job

> serde_json::Value web_submit_batch_scraping_job()
Submit batch scraping job

Submit a batch of URLs for scraping. (Phase 6)

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


## web_take_a_screenshot

> serde_json::Value web_take_a_screenshot()
Take a screenshot

Take a screenshot of a URL. (Phase 2 — patchright engine)

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


## web_web_scraper_health_check

> serde_json::Value web_web_scraper_health_check()
Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes ``/health`` at the root (no ``/api/v1`` prefix, unlike the other scraper services).  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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


## web_web_scraper_health_check_head

> serde_json::Value web_web_scraper_health_check_head()
Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes ``/health`` at the root (no ``/api/v1`` prefix, unlike the other scraper services).  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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

