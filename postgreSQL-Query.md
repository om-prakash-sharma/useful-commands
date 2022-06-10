# Database Common Query 
- List all table with size and record count 
	```
	select table_schema, 
	       table_name, 
	       pg_relation_size(quote_ident(table_name)) ,
	       (xpath('/row/cnt/text()', xml_count))[1]::text::int as row_count
	from (
	  select table_name, table_schema, 
	  query_to_xml(format('select count(*) as cnt from %I.%I', table_schema, table_name), false, true, '') as xml_count
	  from information_schema.tables
	  where table_schema = 'public'
	) subQuery
	```
	
