## forestry_structs

#### This project was created for the integration testing of the schema_generator crate.

- Converts XML file into data structures in Rust (structs) by reading the file forestpropertydata.xml located in the root of the project. The structs are saved in the file src/file_structs.rs.
- Converts XML that is fetched from API into structs and saves the the structs to the file src/url_structs.rs.
- Uses the quick-xml and Serde to read the XML file's data and create a Json file based on the structs.
- Converts the Json file back into XML using a recursive function. The recursive function is not dependent on the structs.

## The generated XML file might have fewer rows than the original XML file:

#### These are not exactly bugs, since the generated file will still contain all the relevant information from the original file.

- <ts:TreeStandDataDate> tags that don't have any content will be written on two rows instead of one.

- The tags and contents inside <gdt:PolygonGeometry> and <gdt:MultiPolygonGeometry> will be written on their own rows, even if they are on a single row in the original XML file.

## License

[MIT License](LICENSE)