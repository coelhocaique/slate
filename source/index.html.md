--- 

title: Personal Finance API 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

APIs to control your personal finance 

**Version:** 1.0.0 

# /DEBT
## ***POST*** 

**Summary:** Add a new debt or something you've spent

### HTTP Request 
`***POST*** /debt` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | successful operation |
| 400 | Invalid request |
| 401 | Unauthorized |
| 500 | Server error |

## ***GET*** 

**Summary:** Find Debts

**Description:** At least one filter should be informed. Reference date range, reference date or reference code

### HTTP Request 
`***GET*** /debt` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| date_from | query | reference date from | No |  |
| date_to | query | reference date to | No |  |
| reference_date | query | reference date | No |  |
| reference_code | query | debt reference code | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid request |
| 401 | Unauthorized |
| 500 | Server error |

## ***DELETE*** 

**Summary:** Delete a Debts

**Description:** Delete by reference code, that means all installments will be deleted

### HTTP Request 
`***DELETE*** /debt` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| reference_code | query | reference date | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | successful operation |
| 400 | Invalid request |
| 401 | Unauthorized |
| 500 | Server error |

# /DEBT/{DEBT_ID}
## ***GET*** 

**Summary:** Find a debt by id

**Description:** Returns a single debt

### HTTP Request 
`***GET*** /debt/{debt_id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| debt_id | path | ID of debt to return | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid request |
| 401 | Unauthorized |
| 500 | Server error |

## ***DELETE*** 

**Summary:** Deletes a debt

### HTTP Request 
`***DELETE*** /debt/{debt_id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| debt_id | path | Debt id to delete | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | successful operation |
| 400 | Invalid request |
| 401 | Unauthorized |
| 500 | Server error |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
