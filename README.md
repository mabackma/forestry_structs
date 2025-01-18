## forestry_structs

#### This project was created for the integration testing of the schema_generator crate.

- Converts XML file into data structures in Rust (structs) by reading the file forestpropertydata.xml located in the root of the project. The structs are saved in the file src/file_structs.rs.
- Converts XML that is fetched from API into structs and saves the the structs to the file src/url_structs.rs.
- Uses the quick-xml and Serde to read the XML file's data and create a Json file based on the structs.
- Converts the Json file back into XML using a recursive function. The recursive function is not dependent on the structs.

## License

[MIT License](LICENSE)