# \FileSanitizationApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**File**](FileSanitizationApi.md#File) | **Post** /cdr/sanitization/file | Complete Content Disarm and Reconstruction on an Input File, and output in same file format
[**FileToPdf**](FileSanitizationApi.md#FileToPdf) | **Post** /cdr/sanitization/file/to/pdf | Complete Content Disarm and Reconstruction on an Input File with PDF/A Output


# **File**
> File(ctx, optional)
Complete Content Disarm and Reconstruction on an Input File, and output in same file format

Processes the input file via CDR to produce a secured output file.  Input content is parsed, disarmed, and then reconstructed into a new output file with the same file format as the input.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***FileSanitizationApiFileOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FileSanitizationApiFileOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **optional.Interface of *os.File**| Input document, or photos of a document, to extract data from | 

### Return type

 (empty response body)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FileToPdf**
> FileToPdf(ctx, optional)
Complete Content Disarm and Reconstruction on an Input File with PDF/A Output

Processes the input file via CDR to produce a secured PDF/A output file.  Input content is parsed, disarmed, and then reconstructed into a new PDF/A output file.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***FileSanitizationApiFileToPdfOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FileSanitizationApiFileToPdfOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **optional.Interface of *os.File**| Input document, or photos of a document, to extract data from | 

### Return type

 (empty response body)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

