## forestry_structs

#### This project was created for the integration testing of the [schema_generator crate](https://github.com/mabackma/schema_generator)

- Converts XML file into data structures in Rust (structs) by reading the file forestpropertydata.xml located in the root of the project. The structs are saved in the file src/file_structs.rs.
- Converts XML that is fetched from API into structs and saves the the structs to the file src/url_structs.rs.
- Uses the quick-xml and Serde to read the XML file's data and create a Json file based on the structs.
- Converts the Json file back into XML using a recursive function. The recursive function is not dependent on the structs.

## The generated XML file might have more rows than the original XML file:

#### When converting from XML to JSON and then back to XML, the generated XML file might have additional rows, even though it contains the correct data from the original file.

- <ts:TreeStandDataDate> tags that don't have any content will be written on two rows instead of one.

- The tags and contents inside <gdt:PolygonGeometry> and <gdt:MultiPolygonGeometry> will be written on their own rows, even if they are on a single row in the original XML file.

## License

[MIT License](LICENSE)
