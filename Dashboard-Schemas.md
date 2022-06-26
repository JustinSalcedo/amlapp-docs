# Dashboard Schema Types

<details>
  <summary><strong>Table of Contents</strong></summary>

  * [Query](#query)
  * [Mutation](#mutation)
  * [Objects](#objects)
    * [AddressType](#addresstype)
    * [AmazonQueryType](#amazonquerytype)
    * [AmazonValueType](#amazonvaluetype)
    * [AmazonVarationType](#amazonvarationtype)
    * [AttributeCombinationDataType](#attributecombinationdatatype)
    * [AttributeDataType](#attributedatatype)
    * [AttributeType](#attributetype)
    * [CurrencyType](#currencytype)
    * [CustomParametersType](#customparameterstype)
    * [CustomSaleTermsType](#customsaletermstype)
    * [DeletedItemsInfoType](#deleteditemsinfotype)
    * [DescriptionDataType](#descriptiondatatype)
    * [DescriptionSnapshotType](#descriptionsnapshottype)
    * [ExtendedFilterIdType](#extendedfilteridtype)
    * [ExtendedFilterType](#extendedfiltertype)
    * [FilterType](#filtertype)
    * [FreeMethodRuleType](#freemethodruletype)
    * [GeoLocationType](#geolocationtype)
    * [IDStringType](#idstringtype)
    * [ItemDataType](#itemdatatype)
    * [ItemDetailsType](#itemdetailstype)
    * [ItemMinimumDetailsType](#itemminimumdetailstype)
    * [ItemType](#itemtype)
    * [LocationType](#locationtype)
    * [MLItemDescriptionType](#mlitemdescriptiontype)
    * [MLMutationType](#mlmutationtype)
    * [MLQueryType](#mlquerytype)
    * [MLValueType](#mlvaluetype)
    * [MLVariationDataType](#mlvariationdatatype)
    * [MLVariationType](#mlvariationtype)
    * [MainImageType](#mainimagetype)
    * [PagingType](#pagingtype)
    * [PictureType](#picturetype)
    * [ProductDetailsType](#productdetailstype)
    * [ReviewType](#reviewtype)
    * [SearchLocationType](#searchlocationtype)
    * [SearchProductDetailsType](#searchproductdetailstype)
    * [SearchResultsType](#searchresultstype)
    * [SellerItemsIDsType](#selleritemsidstype)
    * [ShippingFreeMethodType](#shippingfreemethodtype)
    * [ShippingType](#shippingtype)
    * [SourceDataType](#sourcedatatype)
    * [StageMutationType](#stagemutationtype)
    * [StageQueryType](#stagequerytype)
    * [StagedItem](#stageditem)
    * [StructType](#structtype)
    * [SubValueType](#subvaluetype)
    * [UpdatedItemsInfoType](#updateditemsinfotype)
  * [Inputs](#inputs)
    * [AmazonValueInputType](#amazonvalueinputtype)
    * [AmazonVarationInputType](#amazonvarationinputtype)
    * [AttributeCombinationDataInputType](#attributecombinationdatainputtype)
    * [AttributeDataInputType](#attributedatainputtype)
    * [CurrencyInputType](#currencyinputtype)
    * [CustomSaleTermsInputType](#customsaletermsinputtype)
    * [DescriptionDataInputType](#descriptiondatainputtype)
    * [ItemDataOptionalInputType](#itemdataoptionalinputtype)
    * [ItemMinimumDetailsInputType](#itemminimumdetailsinputtype)
    * [MLVariationInputType](#mlvariationinputtype)
    * [ProductDetailsInputType](#productdetailsinputtype)
    * [SearchOptionsInputType](#searchoptionsinputtype)
    * [SourceDataInputType](#sourcedatainputtype)
  * [Scalars](#scalars)
    * [Boolean](#boolean)
    * [Float](#float)
    * [Int](#int)
    * [String](#string)

</details>

## Query (RootQueryType)
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ml</strong></td>
<td valign="top"><a href="#mlquerytype">MLQueryType</a></td>
<td>Get published items and descriptions</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>amazon</strong></td>
<td valign="top"><a href="#amazonquerytype">AmazonQueryType</a></td>
<td>Find product listings and get item details</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>stage</strong></td>
<td valign="top"><a href="#stagequerytype">StageQueryType</a></td>
<td>Review staged items before publishing them</td>
</tr>
</tbody>
</table>


## Mutation (RootMutationType)
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ml</strong></td>
<td valign="top"><a href="#mlmutationtype">MLMutationType</a></td>
<td>Publish items to Mercado Libre</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>stage</strong></td>
<td valign="top"><a href="#stagemutationtype">StageMutationType</a></td>
<td>Stage, edit, sync, update, and delete items before publishing</td>
</tr>
</tbody>
</table>


## Objects

### AddressType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#locationtype">LocationType</a></td>
<td>City of residence</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#locationtype">LocationType</a></td>
<td>State of residence</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country</strong></td>
<td valign="top"><a href="#locationtype">LocationType</a></td>
<td>Country</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>search_location</strong></td>
<td valign="top"><a href="#searchlocationtype">SearchLocationType</a></td>
<td>Limited location for search</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>latitude</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Latitute coordinates</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>longitude</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Longitude coordinates</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Address ID</td>
</tr>
</tbody>
</table>


### AmazonQueryType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>searchItemsByKeyword</strong></td>
<td valign="top"><a href="#searchresultstype">SearchResultsType</a></td>
<td>Search results for those keywords</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">searchOptions</td>
<td valign="top"><a href="#searchoptionsinputtype">SearchOptionsInputType</a></td>
<td>Additional search options</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getItemsByURL</strong></td>
<td valign="top">[<a href="#itemdetailstype">ItemDetailsType</a>]</td>
<td>A list of details for each item</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">productUrls</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of valid product URLs</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">merchant</td>
<td valign="top"><a href="#string">String</a></td>
<td>Filter by merchant</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getItemByASIN</strong></td>
<td valign="top"><a href="#itemdetailstype">ItemDetailsType</a></td>
<td>Get an item's details using its ASIN</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">asin</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>A valid item's ASIN</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">merchant</td>
<td valign="top"><a href="#string">String</a></td>
<td>Item's merchant</td>
</tr>
</tbody>
</table>


### AmazonValueType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product variation name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dpUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product variation URL</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>selected</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is product variation selected?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is product variation available?</td>
</tr>
</tbody>
</table>


### AmazonVarationType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>variationName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Amazon product variation name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>values</strong></td>
<td valign="top">[<a href="#amazonvaluetype">AmazonValueType</a>]</td>
<td>Variation value</td>
</tr>
</tbody>
</table>


### AttributeCombinationDataType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Attribute combination's name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attibute combination's value ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute combination's value name</td>
</tr>
</tbody>
</table>


### AttributeDataType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Atribute ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute's value name</td>
</tr>
</tbody>
</table>


### AttributeType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute value ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute value name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_struct</strong></td>
<td valign="top"><a href="#structtype">StructType</a></td>
<td>Attribute value structure</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>values</strong></td>
<td valign="top">[<a href="#subvaluetype">SubValueType</a>]</td>
<td>A list of attribute subvalues</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attribute_group_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute group ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attribute_group_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute group name</td>
</tr>
</tbody>
</table>


### CurrencyType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Currency code</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>symbol</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Currency symbol</td>
</tr>
</tbody>
</table>


### CustomParametersType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>profit_margin</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Profit margin over products price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>default_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Default quantity when publshing new items (if available)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>is_profit_percentage</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is the profit margin a percentage? If not, is a fixed margin.</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>buying_mode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Products' buying mode for ML</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>item_condition</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Items' condition when publishing</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>listing_type_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Listing type ID when publishing</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sale_terms</strong></td>
<td valign="top">[<a href="#customsaletermstype">CustomSaleTermsType</a>]</td>
<td>Custom sale terms</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>local_currency_code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Local currency code for ML</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sync_concurrency_in_hours</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Set synchronization concurrency in hours</td>
</tr>
</tbody>
</table>


### CustomSaleTermsType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Sale term ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Sale term value</td>
</tr>
</tbody>
</table>


### DeletedItemsInfoType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ok</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Response code</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>n</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Number of matching items</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deletedCount</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Number of deleted items</td>
</tr>
</tbody>
</table>


### DescriptionDataType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>plain_text</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Description in plain text</td>
</tr>
</tbody>
</table>


### DescriptionSnapshotType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Description snapshot URL</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>width</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Snapshot's width</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>height</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Snapshot's height</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Snapshot status</td>
</tr>
</tbody>
</table>


### ExtendedFilterIdType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>ML search filter ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>field</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Field to filter by</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>missing</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Filter by missing field</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>order</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Sorting parameter</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Filter name</td>
</tr>
</tbody>
</table>


### ExtendedFilterType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#extendedfilteridtype">ExtendedFilterIdType</a></td>
<td>ML advanced search filter</td>
</tr>
</tbody>
</table>


### FilterType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>ML filter ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Filter name</td>
</tr>
</tbody>
</table>


### FreeMethodRuleType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>default</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is this free shiping method default?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>free_mode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Free shipping mode</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>free_shipping_flag</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Free shipping flag</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Free shipping method value</td>
</tr>
</tbody>
</table>


### GeoLocationType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>latitude</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Latitude coordinates</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>longitude</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Longitud coordinates</td>
</tr>
</tbody>
</table>


### IDStringType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>An ID string</td>
</tr>
</tbody>
</table>


### ItemDataType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item title</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subtitle</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item subtitle</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>category_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item category ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Item price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>variations</strong></td>
<td valign="top">[<a href="#mlvariationdatatype">MLVariationDataType</a>]</td>
<td>A list of item variations</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>official_store_id</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Item's official store ID (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currency_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item price's currency</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Item's available stock</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>buying_mode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item buying mode</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>condition</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item's condition</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>listing_type_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item's listing type ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#descriptiondatatype">DescriptionDataType</a></td>
<td>Item description</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>video_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item video ID (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sale_terms</strong></td>
<td valign="top">[<a href="#attributedatatype">AttributeDataType</a>]</td>
<td>Item's sale terms</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pictures</strong></td>
<td valign="top">[<a href="#sourcedatatype">SourceDataType</a>]</td>
<td>A list of item pictures</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attributes</strong></td>
<td valign="top">[<a href="#attributedatatype">AttributeDataType</a>]</td>
<td>A list of item attributes</td>
</tr>
</tbody>
</table>


### ItemDetailsType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>acKeywordLink</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Amazon choice link for the used keyword</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>addon</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is product an addon?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answeredQuestions</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Number of answered questions</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>asin</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product's ASIN</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>categories</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of the product's categories</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countReview</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Number of reviews</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currency</strong></td>
<td valign="top"><a href="#currencytype">CurrencyType</a></td>
<td>Product's price currency</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dealPrice</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Deal price (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deliveryMessage</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Seller's message regarding delivery</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>features</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of the product's features</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fulfilledBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Retailer fulfilling the purchase</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>imageUrlList</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of the product's image URLs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mainImage</strong></td>
<td valign="top"><a href="#mainimagetype">MainImageType</a></td>
<td>Product image for main display</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>manufacturer</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product manufacturer</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minimalQuantity</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Minimal quantity per purchase (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pantry</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is it a pantry product? </td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Product's price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>priceSaving</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Saving price against retail</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>priceShippingInformation</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Shipping cost information</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>prime</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is it a prime product?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productDescription</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product description</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productDetails</strong></td>
<td valign="top">[<a href="#productdetailstype">ProductDetailsType</a>]</td>
<td>A list of product details</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productRating</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product's rating ("x out of y stars)"</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productTitle</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product title</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rentPrice</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Rent price (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>responseMessage</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Request's response message</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>responseStatus</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Request's response status</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>retailPrice</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Product retail price (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>retailPriceRent</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Rent price for retail (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reviews</strong></td>
<td valign="top">[<a href="#reviewtype">ReviewType</a>]</td>
<td>A list of product reviews</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>salePrice</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Sale price (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>shippingPrice</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Product shipping price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>soldBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product's retailer</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>usedPrice</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Used product price (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>variations</strong></td>
<td valign="top">[<a href="#amazonvarationtype">AmazonVarationType</a>]</td>
<td>A list of product variations</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>warehouseAvailability</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product availability in warehouse</td>
</tr>
</tbody>
</table>


### ItemMinimumDetailsType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>asin</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Amazon product's ASIN</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currency</strong></td>
<td valign="top"><a href="#currencytype">CurrencyType</a></td>
<td>Product price's currency</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>features</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of the product's features</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>imageUrlList</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of product image URLs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Product price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productDescription</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product description</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productDetails</strong></td>
<td valign="top">[<a href="#productdetailstype">ProductDetailsType</a>]</td>
<td>A list of product details</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productTitle</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product title</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>variations</strong></td>
<td valign="top">[<a href="#amazonvarationtype">AmazonVarationType</a>]</td>
<td>A list of product variations</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>warehouseAvailability</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product availability in warehouse</td>
</tr>
</tbody>
</table>


### ItemType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>ML ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>site_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Site ID for the selected country</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product title</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subtitle</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Additional product subtitle</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>seller_id</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>ML Seller ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>category_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product category ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>official_store_id</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>ID for an official registered store</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Net price in current currency</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>base_price</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Base price in current currency</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>original_price</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Original price in current currency</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currency_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Currency ID for the current site</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>initial_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Initial stock quantity</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Available stock quantity</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sold_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Sold out stock quantity</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sale_terms</strong></td>
<td valign="top">[<a href="#mlvaluetype">MLValueType</a>]</td>
<td>A list of sale terms</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>buying_mode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product availability status</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>listing_type_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Type of listing ID for the product</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>start_time</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Timestamp of date of publishing</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>stop_time</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Expiration timestamp for the listing</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>condition</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product condition</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permalink</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Listing permanent link</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnail</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Thumbnail image URL</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>secure_thumbnail</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Secure thumbnail image URL</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pictures</strong></td>
<td valign="top">[<a href="#picturetype">PictureType</a>]</td>
<td>A list of product pictures' details</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>video_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product video id (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>descriptions</strong></td>
<td valign="top">[<a href="#idstringtype">IDStringType</a>]</td>
<td>A list of item descriptions' IDs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accepts_mercadopago</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Does product accept Mercado Pago?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>shipping</strong></td>
<td valign="top"><a href="#shippingtype">ShippingType</a></td>
<td>Shipping details</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>international_delivery_mode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>International delivery mode (usually "none")</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>seller_address</strong></td>
<td valign="top"><a href="#addresstype">AddressType</a></td>
<td>Seller address details</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>seller_contact</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Seller contact information</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>location</strong></td>
<td valign="top"><a href="#locationtype">LocationType</a></td>
<td>Location details</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>geolocation</strong></td>
<td valign="top"><a href="#geolocationtype">GeoLocationType</a></td>
<td>Coverage areas</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attributes</strong></td>
<td valign="top">[<a href="#attributetype">AttributeType</a>]</td>
<td>A list of product attributes</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>listing_source</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Original listing source</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>variations</strong></td>
<td valign="top">[<a href="#mlvariationtype">MLVariationType</a>]</td>
<td>A list of product variations</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product activation status</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sub_status</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of product sub-statuses</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of product tags</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>warranty</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product warranty (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>catalog_product_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product catalog ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>domain_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product domain ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parent_items_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Parent item ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>differential_pricing</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Differential pricing (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deal_ids</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of deals' IDs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>automatic_relist</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Activate automatic relist?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>date_created</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Listing creation timestamp</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>last_updated</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Listing update timestamp</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>health</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Listing health score</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>catalog_listing</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is product listed in a catalog?</td>
</tr>
</tbody>
</table>


### LocationType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Location ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Location name</td>
</tr>
</tbody>
</table>


### MLItemDescriptionType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>text</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item description text</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>plain_text</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Description in plain text</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>last_updated</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Timestamp for description's last update</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>date_created</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Description creation's timestamp</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>snapshot</strong></td>
<td valign="top"><a href="#descriptionsnapshottype">DescriptionSnapshotType</a></td>
<td>Description snapshot</td>
</tr>
</tbody>
</table>


### MLMutationType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>publishItemsByID</strong></td>
<td valign="top">[<a href="#itemtype">ItemType</a>]</td>
<td>Publish staged items to ML</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ids</td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of staged item IDs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>publishAll</strong></td>
<td valign="top">[<a href="#itemtype">ItemType</a>]</td>
<td>Publish all the staged items</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>unpublishItemsByID</strong></td>
<td valign="top">[<a href="#itemtype">ItemType</a>]</td>
<td>Unpublish items from ML</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ids</td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of staged item IDs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>unpublishAndDeleteItemsByID</strong></td>
<td valign="top">[<a href="#itemtype">ItemType</a>]</td>
<td>Unpublish items from ML and unstage them</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ids</td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of staged item IDs</td>
</tr>
</tbody>
</table>


### MLQueryType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>getItemsByMLID</strong></td>
<td valign="top">[<a href="#itemtype">ItemType</a>]</td>
<td>Get published items using their ML ID</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ml_ids</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of ML IDs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getAllItemIDs</strong></td>
<td valign="top"><a href="#selleritemsidstype">SellerItemsIDsType</a></td>
<td>Get a list of all items' ML ID for the current seller</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">status</td>
<td valign="top"><a href="#string">String</a></td>
<td>Filter item IDs by listing status</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">sellerSKU</td>
<td valign="top"><a href="#string">String</a></td>
<td>Filter item IDs by the seller's SKU</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getAllItems</strong></td>
<td valign="top">[<a href="#itemtype">ItemType</a>]</td>
<td>Get all published items</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">status</td>
<td valign="top"><a href="#string">String</a></td>
<td>Filter items by publishing status</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">sellerSKU</td>
<td valign="top"><a href="#string">String</a></td>
<td>Fitler items by the seller's SKU</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getItemDescriptionsByMLID</strong></td>
<td valign="top">[<a href="#mlitemdescriptiontype">MLItemDescriptionType</a>]</td>
<td>Item descriptions load separately. Get them by ML ID</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ml_ids</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of ML IDs</td>
</tr>
</tbody>
</table>


### MLValueType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>ML custom data ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>ML data name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>ML data value ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>ML data value name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_struct</strong></td>
<td valign="top"><a href="#structtype">StructType</a></td>
<td>ML data value structure</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>values</strong></td>
<td valign="top">[<a href="#subvaluetype">SubValueType</a>]</td>
<td>A list of ML data subvalues</td>
</tr>
</tbody>
</table>


### MLVariationDataType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>attribute_combinations</strong></td>
<td valign="top">[<a href="#attributecombinationdatatype">AttributeCombinationDataType</a>]</td>
<td>ML attribute combination (data)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Variation price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Available stock for current variation</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attributes</strong></td>
<td valign="top">[<a href="#attributedatatype">AttributeDataType</a>]</td>
<td>A list of variation attributes (data)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sold_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Sold stock for current variation</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>seller_custom_field</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Custom field by seller</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>picture_ids</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of the variation's picture IDs</td>
</tr>
</tbody>
</table>


### MLVariationType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>ML item variation ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Item variation price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attribute_combinations</strong></td>
<td valign="top">[<a href="#mlvaluetype">MLValueType</a>]</td>
<td>A list of the item's attribute combinations</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Available quantity for this variation</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sold_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Quantity of products sold with this variation</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sale_terms</strong></td>
<td valign="top">[<a href="#mlvaluetype">MLValueType</a>]</td>
<td>Variation sale terms</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>picture_ids</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of the variation pictures' ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>seller_custom_field</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Custom field by seller</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>catalog_product_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Variation's catalog ID (if any)</td>
</tr>
</tbody>
</table>


### MainImageType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>imageResolution</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Image resolution in pixels</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>imageUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Image URL</td>
</tr>
</tbody>
</table>


### PagingType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>limit</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Limit of results per page</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>offset</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Results paging offset</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>total</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Total results</td>
</tr>
</tbody>
</table>


### PictureType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Picture ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Picture URL</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>secure_url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Secure picture URL</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>size</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Picture size in pixels</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>max_size</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Maximum picture size in pixels</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>quality</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Image quality (if specified)</td>
</tr>
</tbody>
</table>


### ProductDetailsType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product detail name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product detail value</td>
</tr>
</tbody>
</table>


### ReviewType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>text</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Review text</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>date</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Review date</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rating</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Review rating</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Review title</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Reviewer's username</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Review URL</td>
</tr>
</tbody>
</table>


### SearchLocationType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>neighborhood</strong></td>
<td valign="top"><a href="#locationtype">LocationType</a></td>
<td>Neighborhood of limited search</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#locationtype">LocationType</a></td>
<td>City of limited search</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#locationtype">LocationType</a></td>
<td>State of limited search</td>
</tr>
</tbody>
</table>


### SearchProductDetailsType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>productDescription</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product description</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>asin</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product's ASIN</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countReview</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Product's number of reviews</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>imgUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product's thumbnail URL</td>
</tr>
</tbody>
</table>


### SearchResultsType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>responseStatus</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Search response status</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>responseMessage</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Search response message</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Sorting strategy used</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>domainCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>The specific Amazon domain used</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>keyword</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Search keyword</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>numberOfProducts</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Number of listings</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>foundProducts</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of found products</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>searchProductDetails</strong></td>
<td valign="top">[<a href="#searchproductdetailstype">SearchProductDetailsType</a>]</td>
<td>A list of details for each item found</td>
</tr>
</tbody>
</table>


### SellerItemsIDsType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>seller_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Seller ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>query</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Search by query (using keywords)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paging</strong></td>
<td valign="top"><a href="#pagingtype">PagingType</a></td>
<td>Specify paging parameters</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>results</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of the seller's items' ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>orders</strong></td>
<td valign="top"><a href="#filtertype">FilterType</a></td>
<td>Details for sorting</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available_orders</strong></td>
<td valign="top"><a href="#extendedfiltertype">ExtendedFilterType</a></td>
<td>Available sorting parameters</td>
</tr>
</tbody>
</table>


### ShippingFreeMethodType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Free shipping method ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rule</strong></td>
<td valign="top"><a href="#freemethodruletype">FreeMethodRuleType</a></td>
<td>Rules for free shipping</td>
</tr>
</tbody>
</table>


### ShippingType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>mode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Shipping mode ("not_specified" as default)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>free_methods</strong></td>
<td valign="top">[<a href="#shippingfreemethodtype">ShippingFreeMethodType</a>]</td>
<td>A list of free shipping methods</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>A list of shipping tags</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dimensions</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Shipping dimensions constraint (if specified)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>local_pick_up</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is local pick up available?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>free_shipping</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is shipping free?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>logistic_type</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Logistic type ("not_specified" as default)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>store_pick_up</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is store pick up available?</td>
</tr>
</tbody>
</table>


### SourceDataType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>source</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Picture's source URL</td>
</tr>
</tbody>
</table>


### StageMutationType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>stageItems</strong></td>
<td valign="top">[<a href="#stageditem">StagedItem</a>]</td>
<td>Stage Amazon products to publish in ML</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">amazon_items</td>
<td valign="top">[<a href="#itemminimumdetailsinputtype">ItemMinimumDetailsInputType</a>]!</td>
<td>An array of Amazon products with details for transformation </td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>autoStageItemsByASIN</strong></td>
<td valign="top">[<a href="#stageditem">StagedItem</a>]</td>
<td>Stage Amazon products using only ASINs</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">asins</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of valid product ASINs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateMLInputDataByID</strong></td>
<td valign="top"><a href="#stageditem">StagedItem</a></td>
<td>Update an ML item before publishing</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Item ID</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ml_data</td>
<td valign="top"><a href="#itemdataoptionalinputtype">ItemDataOptionalInputType</a>!</td>
<td>New ML item data</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteItemsByID</strong></td>
<td valign="top"><a href="#deleteditemsinfotype">DeletedItemsInfoType</a></td>
<td>Unstage items by ID</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ids</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of item IDs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>setCustomParameters</strong></td>
<td valign="top"><a href="#customparameterstype">CustomParametersType</a></td>
<td>Set and update the listing parameters for each batch</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">profit_margin</td>
<td valign="top"><a href="#float">Float</a></td>
<td>Profit margin (can be a fixed margin or a percentage)</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">default_quantity</td>
<td valign="top"><a href="#int">Int</a></td>
<td>Default quantity for every availble product in the batch</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">is_profit_percentage</td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is profit margin a percentage? (if not, is a fixed margin)</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">buying_mode</td>
<td valign="top"><a href="#string">String</a></td>
<td>Items' buying mode for ML</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">item_condition</td>
<td valign="top"><a href="#string">String</a></td>
<td>Items' predetermined condition</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">listing_type_id</td>
<td valign="top"><a href="#string">String</a></td>
<td>Listing type ID for the items batch</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">sale_terms</td>
<td valign="top">[<a href="#customsaletermsinputtype">CustomSaleTermsInputType</a>]</td>
<td>Custom sale terms</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">local_currency_code</td>
<td valign="top"><a href="#string">String</a></td>
<td>Uniform local currency code for ML</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">sync_concurrency_in_hours</td>
<td valign="top"><a href="#int">Int</a></td>
<td>Synchronization concurrency in hours</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>turnItemsSyncOn</strong></td>
<td valign="top"><a href="#updateditemsinfotype">UpdatedItemsInfoType</a></td>
<td>Activate items data synchronization</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ids</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of IDs of items to sync</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>turnItemsSyncOff</strong></td>
<td valign="top"><a href="#updateditemsinfotype">UpdatedItemsInfoType</a></td>
<td>Deactivate items data synchronization</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ids</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of IDs of items to unsync</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>syncManuallyByID</strong></td>
<td valign="top">[<a href="#itemtype">ItemType</a>]</td>
<td>Update products data once without auto-sync</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ids</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of item IDs to update from Amazon</td>
</tr>
</tbody>
</table>


### StageQueryType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>getItemsByID</strong></td>
<td valign="top">[<a href="#stageditem">StagedItem</a>]</td>
<td>Get staged items by ID</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">ids</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of item IDs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getItemsByASIN</strong></td>
<td valign="top">[<a href="#stageditem">StagedItem</a>]</td>
<td>Get staged items by their Amazon ASIN</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">asins</td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of valid ASINs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getAllItems</strong></td>
<td valign="top">[<a href="#stageditem">StagedItem</a>]</td>
<td>Get all staged items</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>searchItemsByKeyword</strong></td>
<td valign="top">[<a href="#stageditem">StagedItem</a>]</td>
<td>Search staged items by keywords in product titles</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">keyword</td>
<td valign="top"><a href="#string">String</a>!</td>
<td>An array of keywords</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getAllowedCategoriesIDs</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>Get a list of the allowed ML categories (deprecated)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getPublishedItems</strong></td>
<td valign="top">[<a href="#stageditem">StagedItem</a>]</td>
<td>Get staged items that have been published</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>getNoPublishedItems</strong></td>
<td valign="top">[<a href="#stageditem">StagedItem</a>]</td>
<td>Get unpublished staged items</td>
</tr>
</tbody>
</table>


### StagedItem

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>published_by</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>User who staged the item</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>allow_sync</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is item being synchronized?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ml_data</strong></td>
<td valign="top"><a href="#itemdatatype">ItemDataType</a></td>
<td>Mercado Libre item data</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ml_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Mercado Libre item ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>amazon_data</strong></td>
<td valign="top"><a href="#itemminimumdetailstype">ItemMinimumDetailsType</a></td>
<td>Amazon product data</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item staging timestamp</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item's last update timestamp</td>
</tr>
</tbody>
</table>


### StructType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>number</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td>Struct number</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>unit</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Struct unit</td>
</tr>
</tbody>
</table>


### SubValueType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Subvalue ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Subvalue name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>struct</strong></td>
<td valign="top"><a href="#structtype">StructType</a></td>
<td>Subvalue struct</td>
</tr>
</tbody>
</table>


### UpdatedItemsInfoType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ok</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Response code ("200")</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>n</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Number of matching items</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nModified</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Number of modified items</td>
</tr>
</tbody>
</table>


## Inputs

### AmazonValueInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product variation name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dpUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product variation URL</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>selected</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is product variation selected?</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>Is product variation available?</td>
</tr>
</tbody>
</table>


### AmazonVarationInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>variationName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Variation name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>values</strong></td>
<td valign="top">[<a href="#amazonvalueinputtype">AmazonValueInputType</a>]</td>
<td>A list of values for this Amazon variation</td>
</tr>
</tbody>
</table>


### AttributeCombinationDataInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Attibute combination name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute combination's value ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Attribute combination's value name</td>
</tr>
</tbody>
</table>


### AttributeDataInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Attribute ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Attribute's value name</td>
</tr>
</tbody>
</table>


### CurrencyInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>code</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Currency code</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>symbol</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Currency symbol</td>
</tr>
</tbody>
</table>


### CustomSaleTermsInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Salte term ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value_name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Sale term's value name</td>
</tr>
</tbody>
</table>


### DescriptionDataInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>plain_text</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Description in plain text</td>
</tr>
</tbody>
</table>


### ItemDataOptionalInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item title</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subtitle</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item subtitle</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>category_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item category ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Item price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>variations</strong></td>
<td valign="top">[<a href="#mlvariationinputtype">MLVariationInputType</a>]</td>
<td>An array of item variations</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>official_store_id</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Item's official store (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currency_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item price's currency ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available_quantity</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>Item available stock</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>buying_mode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item buying mode</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>condition</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item condition</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>listing_type_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item's listing type ID</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#descriptiondatainputtype">DescriptionDataInputType</a></td>
<td>Item description</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>video_id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Item's video ID (if any)</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sale_terms</strong></td>
<td valign="top">[<a href="#attributedatainputtype">AttributeDataInputType</a>]</td>
<td>An array of sale terms</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pictures</strong></td>
<td valign="top">[<a href="#sourcedatainputtype">SourceDataInputType</a>]</td>
<td>An array of picture sources</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attributes</strong></td>
<td valign="top">[<a href="#attributedatainputtype">AttributeDataInputType</a>]</td>
<td>An array of attributes data</td>
</tr>
</tbody>
</table>


### ItemMinimumDetailsInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>asin</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Amazon product's ASIN</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currency</strong></td>
<td valign="top"><a href="#currencyinputtype">CurrencyInputType</a></td>
<td>Product price's currency</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>features</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td>An array of the product's features</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>imageUrlList</strong></td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of image URLs</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td>Product price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productDescription</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Product description</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productDetails</strong></td>
<td valign="top">[<a href="#productdetailsinputtype">ProductDetailsInputType</a>]</td>
<td>An array of product details</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>productTitle</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Product title</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>variations</strong></td>
<td valign="top">[<a href="#amazonvarationinputtype">AmazonVarationInputType</a>]</td>
<td>An array of product variations</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>warehouseAvailability</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Product stock in warehouse</td>
</tr>
</tbody>
</table>


### MLVariationInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>attribute_combinations</strong></td>
<td valign="top">[<a href="#attributecombinationdatainputtype">AttributeCombinationDataInputType</a>]!</td>
<td>An array of attribute combinations</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>price</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>Item variation price</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>available_quantity</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>Item available quantity</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attributes</strong></td>
<td valign="top">[<a href="#attributedatainputtype">AttributeDataInputType</a>]!</td>
<td>An array of item's attributes</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sold_quantity</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>Number of sold items</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>seller_custom_field</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Custom field by the seller</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>picture_ids</strong></td>
<td valign="top">[<a href="#string">String</a>]!</td>
<td>An array of picture IDs</td>
</tr>
</tbody>
</table>


### ProductDetailsInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product detail name</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Product detail value</td>
</tr>
</tbody>
</table>


### SearchOptionsInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>keyword</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Search keyword</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>Sorting strategy ["relevanceblender" (default), "price-asc-rank", "price-desc-rank", "review-rank", "date-desc-rank"]</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>page</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>Search results page</td>
</tr>
</tbody>
</table>


### SourceDataInputType

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>source</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>Picture's source URL</td>
</tr>
</tbody>
</table>


## Scalars

### Boolean

The `Boolean` scalar type represents `true` or `false`.

### Float

The `Float` scalar type represents signed double-precision fractional values as specified by [IEEE 754](https://en.wikipedia.org/wiki/IEEE_floating_point).

### Int

The `Int` scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1.

### String

The `String` scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.

