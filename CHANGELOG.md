# ChangeLog

## Overview

This is the changelog for the release of the BWA workflow used for the
ICGC/TCGA PanCancer project.

## Release 2.6.6

* Add ability to upload/download to/from AWS S3 instead of GNOS. To use this feture, added `useGNOS=false` to your INI file. `output_file_url` should be the path to the S3 bucket for upload, for example: `output_file_url=s3://bwa.test.download/` the uploaded files will be `s3://bwa.test.download/merged_output.bam` and `s3://bwa.test.download/merged_output.unmapped.bam`. The `gnos_input_file_url` should still be as `gnos_input_file_url=s3://bwa.test.download/4fb18a5a-9504-11e3-8d90-d1f1d69ccc24,s3://bwa.test.download/9c414428-9446-11e3-86c1-ab5c73f0e08b`, where `4fb18a5a-9504-11e3-8d90-d1f1d69ccc24` and `9c414428-9446-11e3-86c1-ab5c73f0e08b` are directories in the bucket `bwa.test.download`.
* Fixed self-test mode.

## Release 2.6.5

* fixing bug with upload

## Release 2.6.4

* new upload download wrapper

## Release 2.6.3

* removing vcf-uploader now that it is in it own repository

## Release 2.6.2

* Debugging information for GTDownload

## Release 2.6.1

* [PANCANCER-107](https://jira.oicr.on.ca/browse/PANCANCER-107) - Workflow: ensure we can control the maxmemory setting on the unaligned reads extraction steps (new ini param is unmappedReadsJobMemM). These are the only steps that did not have memory params in the ini in the previous version of the workflow.

## Release 2.6.0

You can find these tickets at the OICR JIRA: https://jira.oicr.on.ca. Here are the items addressed in the 2.6.0 release:

* [PANCANCER-6](https://jira.oicr.on.ca/browse/PANCANCER-6) - Metadata: include workflow version string in XML attr
* [PANCANCER-8](https://jira.oicr.on.ca/browse/PANCANCER-8) - Workflow: BAI upload added
* [PANCANCER-9](https://jira.oicr.on.ca/browse/PANCANCER-9) - Workflow: unaligned BAM reads file, separate analysis.xml!
* [PANCANCER-17](https://jira.oicr.on.ca/browse/PANCANCER-17) - per base coverage file
* [PANCANCER-18](https://jira.oicr.on.ca/browse/PANCANCER-18) - Take a pass at cleanup of analysis.xml, there are a few outstanding issues by Keiran
* [PANCANCER-23](https://jira.oicr.on.ca/browse/PANCANCER-23) - Add configurable parameter in ini file for number of children for gtdownload
* [PANCANCER-24](https://jira.oicr.on.ca/browse/PANCANCER-24) - Add more qc metrics using samtools flagstat
* [PANCANCER-25](https://jira.oicr.on.ca/browse/PANCANCER-25) - Failure on pipe fail
* [PANCANCER-32](https://jira.oicr.on.ca/browse/PANCANCER-32) - Add check for valid PI field in BAM headers
* [PANCANCER-33](https://jira.oicr.on.ca/browse/PANCANCER-33) - Add to description
* [PANCANCER-34](https://jira.oicr.on.ca/browse/PANCANCER-34) - Flag to use original quality scores
* [PANCANCER-35](https://jira.oicr.on.ca/browse/PANCANCER-35) - Are we correctly capturing duplicate removal metrics?
* [PANCANCER-39](https://jira.oicr.on.ca/browse/PANCANCER-39) - Analysis Pipeline Section Expansion
* [PANCANCER-42](https://jira.oicr.on.ca/browse/PANCANCER-42) - Broken XML for run.xml
* [PANCANCER-43](https://jira.oicr.on.ca/browse/PANCANCER-43) - Metadata: include workflow runtime into XML key-values
* [PANCANCER-44](https://jira.oicr.on.ca/browse/PANCANCER-44) - Add gtdownload wrapper support for using the timeout parameter
* [PANCANCER-45](https://jira.oicr.on.ca/browse/PANCANCER-45) - Fastq Read Name Checking
* [PANCANCER-47](https://jira.oicr.on.ca/browse/PANCANCER-47) - BAM QC metrics are calculated but never validated
* [PANCANCER-49](https://jira.oicr.on.ca/browse/PANCANCER-49) - BWA workflow, add code to generate md5sum for bai file
* [PANCANCER-51](https://jira.oicr.on.ca/browse/PANCANCER-51) - BWA workflow, upgrade PCAP-core dependent to v1.1.1
* [PANCANCER-52](https://jira.oicr.on.ca/browse/PANCANCER-52) - BWA workflow - track read counts from input BAMs and major workflow steps, error out if reads missed
* [PANCANCER-53](https://jira.oicr.on.ca/browse/PANCANCER-53) - BWA workflow, add step to parse bammarkduplicates metrics report file into JSON and add to Analysis XML
* [PANCANCER-56](https://jira.oicr.on.ca/browse/PANCANCER-56) - Evaluate other reference files to add to Workflow
