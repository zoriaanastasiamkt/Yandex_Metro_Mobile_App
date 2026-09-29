# Yandex_Metro_Mobile_App
QA project: functional and regression testing of Yandex Metro Android application.

## Project Overview

This project focuses on functional and regression testing of the Yandex Metro Android application following a code refactoring.

The goal was to verify the updated functionality, check that existing features continued to work correctly, identify defects, and assess the readiness of the new version for release.

The current version (2.13) was used as a reference, and the new version (3.6) was tested against the provided requirements.

## Project Objectives

* Analyze the requirements affected by the refactoring.
* Create functional test checklists for the updated features.
* Prepare a regression checklist covering mobile-specific scenarios.
* Execute test cases and document the results.
* Report defects with steps to reproduce and supporting evidence.
* Prepare a test report with release recommendations.

## Test Environment

| Parameter          | Details                                         |
| ------------------ | ----------------------------------------------- |
| Application        | Yandex Metro for Android                        |
| Version under test | 3.6                                             |
| Reference version  | 2.13                                            |
| Device             | Android Studio Emulator (Honor 8 configuration) |
| Operating system   | Android 9.0 Pie                                 |
| Screen resolution  | 1080 × 1920                                     |
| Screen size        | 5.5 inches                                      |

## Testing Scope

### Functional Testing

* Testing functionality affected by the refactoring.
* Checking application behavior against the provided requirements.
* Verifying route-building functionality and related features.

### Regression Testing

* Checking existing application functionality.
* Testing mobile-specific behavior and interactions.
* Verifying application behavior under different conditions.

### Defect Reporting

Defects were documented with identifiers, descriptions, and supporting evidence, including screenshots and screen recordings where applicable.

## Tools and Technologies

* Android Studio Emulator — mobile application testing.
* Microsoft Excel / Google Sheets — test checklists, test execution results, and bug reports.
* Android APK — installation and testing of application versions.
* Yandex Metro requirements document (PDF) — requirements analysis and test design.

**Testing types:** Manual testing, functional testing, regression testing, mobile testing, and exploratory checks.

## Project Structure

```text
yandex-metro-qa/
├── README.md
├── test-documentation/
   ├── Yandex_Metro_Check_lists_Bug_Report.xlsx
   └── Yandex_Metro_App_Report.docx

```

### Files and Directories

* `README.md` — project overview, testing scope, tools, and results.
* `test-documentation/` — functional and regression checklists, bug reports, and the final test report.

## Test Results

A total of 69 checks were executed:

| Test type          | Checks |
| ------------------ | -----: |
| Functional testing |     35 |
| Regression testing |     34 |
| **Total**          | **69** |

| Result | Number |
| ------ | -----: |
| Passed |     48 |
| Failed |     21 |

### Defects by Priority

* Critical: BUG-3, BUG-13, BUG-15.
* High: BUG-1, BUG-2, BUG-11, BUG-14.
* Low: BUG-4 through BUG-10, BUG-12.

### Key Findings

The following critical defects were identified:

1. The time interval does not update automatically, which may result in outdated route information.
2. Routes can be built without an internet connection, without displaying an appropriate error message.
3. The feedback button redirects users to a mail server instead of opening the in-app support interface.

## Conclusion and Recommendations

The testing revealed critical defects that should be fixed before the release of version 3.6.

After the fixes, the affected functionality should be retested, followed by regression testing of route building, time interval updates, offline behavior, and the feedback feature.

The test results and defect details are documented in the attached Excel file and test report.

## How to Run the Tests

1. Install Android Studio and configure an Android 9.0 (API 28) emulator.
2. Configure the emulator to match the Honor 8 test environment, with a resolution of 1080 × 1920.
3. Obtain the application APK files:

   * [Yandex Metro v2.13 — reference version](https://code.s3.yandex.net/qa/files/yandexmetro-android-v2.13.apk)
   * [Yandex Metro v3.6 — version under test](https://code.s3.yandex.net/qa/files/yandexmetro-android-v3.6.apk)
4. Install the required APK on the emulator.
5. Execute the functional and regression checks listed in the Excel file.
6. Record the results and report any defects.

## System Requirements

* Android Studio with Android Emulator.
* Android 9.0 (API 28) system image.
* Emulator configured to match the specified device resolution.
* Yandex Metro APK version 3.6.
* Excel or a compatible spreadsheet application to view the test documentation.

## Author

Anastasia Zoria
