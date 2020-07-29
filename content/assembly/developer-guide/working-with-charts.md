---
id: "working-with-charts"
url: "assembly/working-with-charts"
title: "Working With Charts"
productName: "GroupDocs.Assembly Cloud"
weight: 4
description: ""
keywords: ""
---






# Multiple Types of Charts in Microsoft Word Document #

GroupDocs.Assembly Cloud REST APIs for document assembling with many features such as Template Syntax, Manipulate Data using Formulae & Sequential Data Operations, Variables, Generate Barcode Image, Change File Format of the Assembled Document for multiple supported formats with XML & JSON data. To build report with charts, You can use the below steps for template & data with Assembly Build API.

## Creating a Template ##

Please follow below steps to create a chart template in MS Word 2013:

1. Click in the document where you want to insert the chart, click the "Insert" tab, then click "Chart" in the illustrations group to open the "Insert Chart" dialog box.
1. Select "X Y(Scatter)" in the sidebar, you will see a gallery of charts.
1. Select the e.g "Bubble" and press "OK" to insert the chart and Worksheet template to your document.
1. Right click the chart and select 'Edit Data' to provide chart data. See [Data (JSON)]("Template Syntax for GroupDocs.Assembly Engine")
1. Save your Document.

### Template Syntax ###





 GroupDocs.Assembly Engine Template Syntax

```html 
 '
<
<[team1Name]>>' vs.'
<
<[team2Name]>>' match stats
<
<foreach [in quarterStats]>>
<
<x [quarter + "Q"]>>
 ```




 Data (JSON)

```html 
{
  "matchStats": {
    "QuarterStats": [
      {
        "Quarter": 1,
        "Team1Stats": {
          "Pct3Pt": 36.7,
          "PctFg": 45.3,
          "Points": 27
        },
        "Team2Stats": {
          "Pct3Pt": 35.5,
          "PctFg": 44.0,
          "Points": 23
        }
      },
      {
        "Quarter": 2,
        "Team1Stats": {
          "Pct3Pt": 33.0,
          "PctFg": 40.5,
          "Points": 21
        },
        "Team2Stats": {
          "Pct3Pt": 34.0,
          "PctFg": 41.7,
          "Points": 26
        }
      },
      {
        "Quarter": 3,
        "Team1Stats": {
          "Pct3Pt": 39.1,
          "PctFg": 42.0,
          "Points": 33
        },
        "Team2Stats": {
          "Pct3Pt": 25.9,
          "PctFg": 35.9,
          "Points": 25
        }
      },
      {
        "Quarter": 4,
        "Team1Stats": {
          "Pct3Pt": 35.1,
          "PctFg": 43.5,
          "Points": 29
        },
        "Team2Stats": {
          "Pct3Pt": 36.5,
          "PctFg": 51.0,
          "Points": 33
        }
      }
    ],
    "Team1Name": "Cleveland Cavaliers",
    "Team2Name": "Golden State Warriors"
  }
}
 ```







For detailed technical information about syntax, expressions and report generation by the engine, please visit: .


### Download Resources ###

Please download the sample template document we created in this article:

* [All Chart Types.docx](https://github.com/groupdocs-assembly-cloud/groupdocs-assembly-cloud-dotnet-samples/blob/master/Examples/Data/Assembler/TestAllChartTypes.docx) (Template for JSON examples)
* [Data.json](https://github.com/groupdocs-assembly-cloud/groupdocs-assembly-cloud-dotnet-samples/blob/master/Examples/Data/Assembler/Teams.json) (JSON data examples)

## API Resource ##

The following GroupDocs.Assembly Cloud REST API resource has been used in the [Build Reports](https://apireference.groupdocs.cloud/assembly/#/assembly/build) example.

## cURL Example ##





 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1/assembly/TestAllChartTypes.docx/build" -X POST  -H "Content-Type: application/json" -H "authorization: Bearer [Access Token]" -f "saveOptions#{'SaveFormat':'docx'}" -f "matchStats#{"matchStats":{'QuarterStats':[{'Quarter':1,'Team1Stats':{'Pct3Pt':36.7,'PctFg':45.3,'Points':27},'Team2Stats':{'Pct3Pt':35.5,'PctFg':44.0,'Points':23}},{'Quarter':2,'Team1Stats':{'Pct3Pt':33.0,'PctFg':40.5,'Points':21},'Team2Stats':{'Pct3Pt':34.0,'PctFg':41.7,'Points':26}},{'Quarter':3,'Team1Stats':{'Pct3Pt':39.1,'PctFg':42.0,'Points':33},'Team2Stats':{'Pct3Pt':25.9,'PctFg':35.9,'Points':25}},{'Quarter':4,'Team1Stats':{'Pct3Pt':35.1,'PctFg':43.5,'Points':29},'Team2Stats':{'Pct3Pt':36.5,'PctFg':51.0,'Points':33}}],'Team1Name':'Cleveland Cavaliers','Team2Name':'Golden State Warriors'}}" 
 ```




 Response

```html 
{
  "Code": 200,
  "Status": "OK"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-assembly-cloud).





 C#




{{< gist groupdocscloud d194ffc596a42eefca1757e32c6bf392 Assembly_CSharp_Charts_Word_Processing_Document.cs
 >}}









# Multiple Types of Charts in PDF #

GroupDocs.Assembly Cloud REST APIs for document assembling with many features such as Template Syntax, Manipulate Data using Formulae & Sequential Data Operations, Variables, Generate Barcode Image, Change File Format of the Assembled Document for multiple supported formats with XML & JSON data. To build report with charts, You can use the below steps for template & data with Assembly Build API.

## Creating a Template ##

Please follow below steps to create a chart template in MS Word 2013:

1. Click in the document where you want to insert the chart, click the "Insert" tab, then click "Chart" in the illustrations group to open the "Insert Chart" dialog box.
1. Select "X Y(Scatter)" in the sidebar, you will see a gallery of charts.
1. Select the e.g "Bubble" and press "OK" to insert the chart and Worksheet template to your document.
1. Right click the chart and select 'Edit Data' to provide chart data. See [Data (JSON)]("Template Syntax for GroupDocs.Assembly Engine")
1. Save your Document.

### Template Syntax ###





 GroupDocs.Assembly Engine Template Syntax

```html 
 '
<
<[team1Name]>>' vs.'
<
<[team2Name]>>' match stats
<
<foreach [in quarterStats]>>
<
<x [quarter + "Q"]>>
 ```




 Data (JSON)

```html 
{
  "matchStats": {
    "QuarterStats": [
      {
        "Quarter": 1,
        "Team1Stats": {
          "Pct3Pt": 36.7,
          "PctFg": 45.3,
          "Points": 27
        },
        "Team2Stats": {
          "Pct3Pt": 35.5,
          "PctFg": 44.0,
          "Points": 23
        }
      },
      {
        "Quarter": 2,
        "Team1Stats": {
          "Pct3Pt": 33.0,
          "PctFg": 40.5,
          "Points": 21
        },
        "Team2Stats": {
          "Pct3Pt": 34.0,
          "PctFg": 41.7,
          "Points": 26
        }
      },
      {
        "Quarter": 3,
        "Team1Stats": {
          "Pct3Pt": 39.1,
          "PctFg": 42.0,
          "Points": 33
        },
        "Team2Stats": {
          "Pct3Pt": 25.9,
          "PctFg": 35.9,
          "Points": 25
        }
      },
      {
        "Quarter": 4,
        "Team1Stats": {
          "Pct3Pt": 35.1,
          "PctFg": 43.5,
          "Points": 29
        },
        "Team2Stats": {
          "Pct3Pt": 36.5,
          "PctFg": 51.0,
          "Points": 33
        }
      }
    ],
    "Team1Name": "Cleveland Cavaliers",
    "Team2Name": "Golden State Warriors"
  }
}
 ```







For detailed technical information about syntax, expressions and report generation by the engine, please visit: .


### Download Resources ###

Please download the sample template document we created in this article:

* [All Chart Types.docx](https://github.com/groupdocs-assembly-cloud/groupdocs-assembly-cloud-dotnet-samples/blob/master/Examples/Data/Assembler/TestAllChartTypes.docx) (Template for JSON examples)
* [Data.json](https://github.com/groupdocs-assembly-cloud/groupdocs-assembly-cloud-dotnet-samples/blob/master/Examples/Data/Assembler/Teams.json) (JSON data examples)

## API Resource ##

The following GroupDocs.Assembly Cloud REST API resource has been used in the [Build Reports](https://apireference.groupdocs.cloud/assembly/#/assembly/build) example.

## cURL Example ##





 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1/assembly/TestAllChartTypes.docx/build" -X POST  -H "Content-Type: application/json" -H "authorization: Bearer [Access Token]" -f "saveOptions#{'SaveFormat':'pdf'}" -f "matchStats#{"matchStats":{'QuarterStats':[{'Quarter':1,'Team1Stats':{'Pct3Pt':36.7,'PctFg':45.3,'Points':27},'Team2Stats':{'Pct3Pt':35.5,'PctFg':44.0,'Points':23}},{'Quarter':2,'Team1Stats':{'Pct3Pt':33.0,'PctFg':40.5,'Points':21},'Team2Stats':{'Pct3Pt':34.0,'PctFg':41.7,'Points':26}},{'Quarter':3,'Team1Stats':{'Pct3Pt':39.1,'PctFg':42.0,'Points':33},'Team2Stats':{'Pct3Pt':25.9,'PctFg':35.9,'Points':25}},{'Quarter':4,'Team1Stats':{'Pct3Pt':35.1,'PctFg':43.5,'Points':29},'Team2Stats':{'Pct3Pt':36.5,'PctFg':51.0,'Points':33}}],'Team1Name':'Cleveland Cavaliers','Team2Name':'Golden State Warriors'}}" 
 ```




 Response

```html 
{
  "Code": 200,
  "Status": "OK"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-assembly-cloud).





 C#




{{< gist groupdocscloud d194ffc596a42eefca1757e32c6bf392 Assembly_CSharp_Charts_PDF.cs
 >}}







