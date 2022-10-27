# ACCESS CONECT Information Sharing Platform
# Drupal Feed of ACCESS Integrated Resources

## Summary

Mirrors Basic Information about ACCESS Active RP Resources into a Drupal content type.

Includes a URL for retrieving all available CiDeR information in JSON format.

Information comes from an Information Sharing Platform API with built-in filters defining ACCESS Active.

## Basic Information

Basic information includes:
- Resource Descriptive Name (Title)
- Detail View URL - link to a public CiDeR page of the resource
- Raw Data URL - link to a public API returning all availailble resource information in JSON
- Resource type
- Latest resource status, begin and end dates
- Organization name, URL, and logo URL
- Affiliation, XSEDE for now, eventually ACCESS
- CiDeR Resource ID 
- Global Information Sharing Platform Resource ID

## Implementation Details

Creates these Drupal elements:
- Content Type: ACCESS Active Resources from CiDeR
  Machine name: access_active_resources_from_cid

- Feed Type: ACCESS Active Resources from CiDeR Feed
  Machine name: cider_active_resources_feed

- Feed: Retrieve CiDeR from Operations API


Developed and tested using:
- Drupal 9.4.8

- Feeds 8.x-3.0-beta2
  https://www.drupal.org/project/feeds

- Feeds Extensible Parsers 8.x-1.0-beta1
  https://www.drupal.org/project/feeds_ex


## Developer Notes

1. Full Drupal export before implementation
2. Define Content Tyupe, Feed Type, Feed
3. Full Drupal export after implementation
4. tar -C export_after -czvf new_files.tgz `diff -n export_before export_after|awk '{print $4}'`
5. extrac new_files.tgz into the export/ directory
