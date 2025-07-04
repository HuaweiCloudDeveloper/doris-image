<p align="center">
  <h1 align="center">Doris Database</h1>
  <p align="center">
    <strong>English</strong> | <a href="README_ZH.md">简体中文</a>
  </p>

## Table of Contents

- [Repository Introduction](#project-introduction)
- [Prerequisites](#prerequisites)
- [Image Description](#image-description)
- [Getting Help](#getting-help)
- [How to Contribute](#how-to-contribute)

## Project Introduction
[Apache Doris](https://github.com/apache/doris) is a high-performance, real-time analytical database based on the MPP architecture. It is well-known for its efficiency, simplicity, and unity. It can return query results for massive data in sub-second response times. It can support both high-concurrency point query scenarios and high-throughput complex analysis scenarios. Based on this, Apache Doris can well meet usage scenarios such as report analysis, ad-hoc query, unified data warehouse construction, and data lakehouse integration. Users can build applications such as large-screen dashboards, user behavior analysis, AB testing platforms, log retrieval analysis, user portrait analysis, and order analysis on top of it.

**Use cases of Apache Doris:**
- Report analysis
    - Real-time dashboards;
    - Reports for internal enterprise analysts and managers;
    - High-concurrency report analysis for users or customers (Customer Facing Analytics). For example, site analysis for website owners and advertising reports for advertisers. Usually, concurrency requires tens of thousands of QPS, and query latency requires millisecond-level response. The well-known e-commerce company JD.com uses Apache Doris in its advertising reports, writing 10 billion rows of data per day, with a query concurrency QPS of over ten thousand and a 99th percentile query latency of 150ms.
- Ad-hoc Query: Self-service analysis for analysts with non-fixed query patterns, requiring high throughput. Xiaomi built a Growth Analytics (GA) platform based on Apache Doris, using user behavior data for business growth analysis. The average query latency is 10s, the 95th percentile query latency is within 30s, and the daily SQL query volume is tens of thousands.
- Data Lakehouse: Federated analysis of data in offline lakehouses such as Hive, Iceberg, and Hudi through external tables, significantly improving query performance without data copying.
- Log retrieval analysis: In the Apache Doris 2.0 version, inverted indexes and full-text retrieval are supported, which can well meet the log retrieval analysis scenario. Relying on its efficient query engine and storage engine, it has a 10-fold cost-performance advantage compared to traditional log retrieval analysis solutions.
- Unified data warehouse construction: One platform meets the unified data warehouse construction needs, simplifying the cumbersome big data software stack. Haidilao built a unified data warehouse based on Apache Doris, replacing the old architecture composed of Spark, Hive, Kudu, Hbase, and Phoenix, greatly simplifying the architecture.

This project provides an open-source mirror product [**Doris Database**](https://marketplace.huaweicloud.com/intl/hidden/contents/642304b4-117e-4c88-b79f-933a7d861599), which has Doris and its related operating environments pre-installed and provides deployment templates. Come and refer to the usage guide to easily start the "out-of-the-box" efficient experience!

> **System requirements are as follows:**
> - CPU: 2GHz or higher
> - RAM: 8GB or larger
> - Disk: At least 40GB

## Prerequisites
[Register a Huawei account and activate Huawei Cloud](https://support.huaweicloud.com/usermanual-account/account_id_001.html)

## Image Description

| Image Specification           | Feature Description                                           | Remarks |
|-------------------------------|------------------------------------------------| --- |
| [doris-2.1.10-kunpeng](https://github.com/HuaweiCloudDeveloper/doris-image/tree/doris-2.1.10-kunpeng) | Installed and deployed based on Kunpeng servers + Huawei Cloud EulerOS 2.0 64-bit |  |

## Getting Help
- For more questions, you can contact us through [issues](https://github.com/HuaweiCloudDeveloper/doris-image/issues) or the service support of the specified product on the Huawei Cloud Marketplace.
- For other open-source images, see [open-source-image-repos](https://github.com/HuaweiCloudDeveloper/open-source-image-repos)

## How to Contribute
- Fork this repository and submit a merge request.
- Synchronously update README.md based on your open-source image information.
