V1.3.4 [Custom]

- Based on AWS SDK V2
- Refactored query_filter to filter_expressions so that we can use projection_expressions instead of attributes_to_get in querying
- To select only specific attributes, even nested json ones, pass an array of string params of the desired atributes into .project()
- E.g. Model.where(identifier: 'AT-SOMETHING', created_at: some_time).project(['message.gnss', 'message.battery']).all
