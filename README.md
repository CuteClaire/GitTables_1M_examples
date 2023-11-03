# GitTables_1M_examples
## .parquet
一个parquet文件由 **metadata** + **table** 组成
### metadata
原文件metadata无换行和缩进，整理为含换行与缩进样式

在本例子中整理为metadata.txt:
```
{
    "gittables": 
        "{
            \"license\": \"MIT License\", 
            \"csv_url\": \"https://github.com/alixaxel/dump.HN/blob/11fd7291c89c68daf4196a47e8cfa47e4df30c8d/data/items/2007/07/17/00-01.csv\", 
            \"dtypes\": 
                {
                    \"ID\": \"int64\", 
                    \"Type\": \"object\", 
                    \"Story\": \"float64\", 
                    \"Parent\": \"float64\", 
                    \"Points\": \"int64\", 
                    \"Comments\": \"int64\", 
                    \"Author\": \"object\", 
                    \"Title\": \"object\", 
                    \"URL\": \"object\", 
                    \"Content\": \"object\", 
                    \"Created\": \"int64\"
                },
            \"number_rows\": 10, 
            \"number_columns\": 11, 
            \"dtypes_percentages\": 
                {
                    \"int64\": 0.36363636363636365, 
                    \"object\": 0.45454545454545453, 
                    \"float64\": 0.18181818181818182
                }, 
            \"dbpedia_syntactic_column_types\": 
                {
                    \"Author\": 
                        {
                            \"cleaned_label\": \"author\", 
                            \"description\": null, 
                            \"domain\": [\"http://dbpedia.org/ontology/Work\"], 
                            \"id\": \"http://dbpedia.org/ontology/author\", 
                            \"range\": [\"http://dbpedia.org/ontology/Person\"], 
                            \"superproperty\": [\"http://www.ontologydesignpatterns.org/ont/dul/DUL.owl#coparticipatesWith\"]
                        },
                    \"Created\": 
                        {
                            \"cleaned_label\": \"created\",
                            \"description\": null, 
                            \"domain\": [\"http://dbpedia.org/ontology/Person\"],
                            \"id\": \"http://dbpedia.org/ontology/created\",
                            \"range\": [\"http://dbpedia.org/ontology/Work\"], 
                            \"superproperty\": null
                        }, 
                    \"ID\": 
                        {
                            \"cleaned_label\": \"id\", 
                            \"description\": null, 
                            \"domain\": [\"http://dbpedia.org/ontology/WorldHeritageSite\"], 
                            \"id\": \"http://dbpedia.org/ontology/id\", 
                            \"range\": [\"http://www.w3.org/2001/XMLSchema#string\"], 
                            \"superproperty\": null
                        }, 
                    \"Parent\": 
                        {
                            \"cleaned_label\": \"parent\", 
                            \"description\": null, 
                            \"domain\": [\"http://dbpedia.org/ontology/Person\"], 
                            \"id\": \"http://dbpedia.org/ontology/parent\", 
                            \"range\": [\"http://dbpedia.org/ontology/Person\"], 
                            \"superproperty\": [\"http://www.ontologydesignpatterns.org/ont/dul/DUL.owl#sameSettingAs\"]
                        }, 
                    \"Title\": 
                        {
                            \"cleaned_label\": \"title\", 
                            \"description\": null, 
                            \"domain\": null, 
                            \"id\": \"http://dbpedia.org/ontology/title\", 
                            \"range\": [\"http://www.w3.org/1999/02/22-rdf-syntax-ns#langString\"],
                            \"superproperty\": null
                        }, 
                    \"Type\": 
                        {
                            \"cleaned_label\": \"type\", 
                            \"description\": null, 
                            \"domain\": null, 
                            \"id\": \"http://dbpedia.org/ontology/type\", 
                            \"range\": null, 
                            \"superproperty\": [\"http://www.ontologydesignpatterns.org/ont/dul/DUL.owl#isClassifiedBy\"]
                        }
                }, 
            \"schema_syntactic_column_types\": 
                {
                    \"Author\": 
                        {
                            \"id\": \"schema:author\", 
                            \"cleaned_label\": \"author\", 
                            \"description\": \"The author of this content or rating. Please note that author is special in that HTML 5 provides a special mechanism for indicating authorship via the rel tag. That is equivalent to this and may be used interchangeably.\", 
                            \"type\": \"rdf:Property\", 
                            \"domain\": 
                                [
                                    \"schema:CreativeWork\", 
                                    \"schema:Rating\"
                                ], 
                            \"range\": 
                                [
                                    \"schema:Person\", 
                                    \"schema:Organization\"
                                ], 
                            \"superclasses\": null, 
                            \"superproperties\": null
                        }, 
                    \"ID\": 
                        {
                            \"id\": \"schema:identifier\", 
                            \"cleaned_label\": \"id\", 
                            \"description\": \"The identifier property represents any kind of identifier for any kind of [[Thing]], such as ISBNs, GTIN codes, UUIDs etc. Schema.org provides dedicated properties for representing many of these, either as textual strings or as URL (URI) links. See [background notes](/docs/datamodel.html#identifierBg) for more details.\\n        \", 
                            \"type\": \"rdf:Property\", 
                            \"domain\": [\"schema:Thing\"], 
                            \"range\": [\"schema:PropertyValue\", 
                            \"schema:URL\", \"schema:Text\"], 
                            \"superclasses\": null, 
                            \"superproperties\": null
                        }, 
                    \"Parent\": 
                        {
                            \"id\": \"schema:parent\", 
                            \"cleaned_label\": \"parent\", 
                            \"description\": \"A parent of this person.\",
                            \"type\": \"rdf:Property\", 
                            \"domain\": [\"schema:Person\"], 
                            \"range\": [\"schema:Person\"], 
                            \"superclasses\": null, 
                            \"superproperties\": null
                        }, 
                    \"Title\": 
                        {
                            \"id\": \"schema:title\", 
                            \"cleaned_label\": \"title\", 
                            \"description\": \"The title of the job.\", 
                            \"type\": \"rdf:Property\", 
                            \"domain\": [\"schema:JobPosting\"], 
                            \"range\": [\"schema:Text\"], 
                            \"superclasses\": null, 
                            \"superproperties\": null
                        }, 
                    \"URL\": 
                        {
                            \"id\": \"schema:URL\", 
                            \"cleaned_label\": \"url\", 
                            \"description\": \"Data type: URL.\", 
                            \"type\": \"rdfs:Class\", \
                            "domain\": null, 
                            \"range\": null, 
                            \"superclasses\": [\"schema:Text\"], 
                            \"superproperties\": null
                        }
                }, 
            \"dbpedia_semantic_column_types\": 
                {
                    \"ID\": {\"cleaned_label\": \"id\", \"description\": null, \"domain\": [\"http://dbpedia.org/ontology/WorldHeritageSite\"], \"id\": \"http://dbpedia.org/ontology/id\", \"range\": [\"http://www.w3.org/2001/XMLSchema#string\"], \"superproperty\": null}, \"Type\": {\"cleaned_label\": \"type\", \"description\": null, \"domain\": null, \"id\": \"http://dbpedia.org/ontology/type\", \"range\": null, \"superproperty\": [\"http://www.ontologydesignpatterns.org/ont/dul/DUL.owl#isClassifiedBy\"]}, \"Story\": {\"cleaned_label\": \"story editor\", \"description\": null, \"domain\": [\"http://dbpedia.org/ontology/TelevisionShow\"], \"id\": \"http://dbpedia.org/ontology/storyEditor\", \"range\": [\"http://dbpedia.org/ontology/Person\"], \"superproperty\": [\"http://www.ontologydesignpatterns.org/ont/dul/DUL.owl#sameSettingAs\"]}, \"Parent\": {\"cleaned_label\": \"parent\", \"description\": null, \"domain\": [\"http://dbpedia.org/ontology/Person\"], \"id\": \"http://dbpedia.org/ontology/parent\", \"range\": [\"http://dbpedia.org/ontology/Person\"], \"superproperty\": [\"http://www.ontologydesignpatterns.org/ont/dul/DUL.owl#sameSettingAs\"]}, \"Points\": {\"cleaned_label\": \"career points\", \"description\": null, \"domain\": [\"http://dbpedia.org/ontology/FormulaOneRacer\"], \"id\": \"http://dbpedia.org/ontology/careerPoints\", \"range\": [\"http://www.w3.org/2001/XMLSchema#integer\"], \"superproperty\": null}, \"Comments\": {\"cleaned_label\": \"comment\", \"description\": null, \"domain\": null, \"id\": \"http://dbpedia.org/ontology/comment\", \"range\": [\"http://www.w3.org/2001/XMLSchema#string\"], \"superproperty\": null}, \"Author\": {\"cleaned_label\": \"author\", \"description\": null, \"domain\": [\"http://dbpedia.org/ontology/Work\"], \"id\": \"http://dbpedia.org/ontology/author\", \"range\": [\"http://dbpedia.org/ontology/Person\"], \"superproperty\": [\"http://www.ontologydesignpatterns.org/ont/dul/DUL.owl#coparticipatesWith\"]}, \"Title\": {\"cleaned_label\": \"title\", \"description\": null, \"domain\": null, \"id\": \"http://dbpedia.org/ontology/title\", \"range\": [\"http://www.w3.org/1999/02/22-rdf-syntax-ns#langString\"], \"superproperty\": null}, \"URL\": {\"cleaned_label\": \"file url\", \"description\": null, \"domain\": [\"http://dbpedia.org/ontology/File\"], \"id\": \"http://dbpedia.org/ontology/fileURL\", \"range\": [\"http://dbpedia.org/ontology/File\"], \"superproperty\": null}, \"Content\": {\"cleaned_label\": \"open access content\", \"description\": \"Availability of open access content.\", \"domain\": [\"http://dbpedia.org/ontology/PeriodicalLiterature\"], \"id\": \"http://dbpedia.org/ontology/openAccessContent\", \"range\": [\"http://www.w3.org/2001/XMLSchema#string\"], \"superproperty\": null}, \"Created\": {\"cleaned_label\": \"created\", \"description\": null, \"domain\": [\"http://dbpedia.org/ontology/Person\"], \"id\": \"http://dbpedia.org/ontology/created\", \"range\": [\"http://dbpedia.org/ontology/Work\"], \"superproperty\": null}
                }, 
            \"dbpedia_semantic_similarities\": 
                {
                    \"ID\": 1.0, \"Type\": 1.0, \"Story\": 0.7859, \"Parent\": 1.0, \"Points\": 0.7756, \"Comments\": 0.792, \"Author\": 1.0, \"Title\": 1.0, \"URL\": 0.7583, \"Content\": 0.6709, \"Created\": 1.0
                }, 
            \"schema_semantic_column_types\": 
                {
                    \"ID\": 
                        {
                            \"id\": \"schema:identifier\", \"cleaned_label\": \"id\", \"description\": \"The identifier property represents any kind of identifier for any kind of [[Thing]], such as ISBNs, GTIN codes, UUIDs etc. Schema.org provides dedicated properties for representing many of these, either as textual strings or as URL (URI) links. See [background notes](/docs/datamodel.html#identifierBg) for more details.\\n        \", \"type\": \"rdf:Property\", \"domain\": [\"schema:Thing\"], \"range\": [\"schema:PropertyValue\", \"schema:URL\", \"schema:Text\"], \"superclasses\": null, \"superproperties\": null}, \"Type\": {\"id\": \"schema:procedureType\", \"cleaned_label\": \"procedure type\", \"description\": \"The type of procedure, for example Surgical, Noninvasive, or Percutaneous.\", \"type\": \"rdf:Property\", \"domain\": [\"schema:MedicalProcedure\"], \"range\": [\"schema:MedicalProcedureType\"], \"superclasses\": null, \"superproperties\": null}, \"Story\": {\"id\": \"schema:ShortStory\", \"cleaned_label\": \"short story\", \"description\": \"Short story or tale. A brief work of literature, usually written in narrative prose.\", \"type\": \"rdfs:Class\", \"domain\": null, \"range\": null, \"superclasses\": [\"schema:CreativeWork\"], \"superproperties\": null}, \"Parent\": {\"id\": \"schema:parent\", \"cleaned_label\": \"parent\", \"description\": \"A parent of this person.\", \"type\": \"rdf:Property\", \"domain\": [\"schema:Person\"], \"range\": [\"schema:Person\"], \"superclasses\": null, \"superproperties\": null}, \"Points\": {\"id\": \"schema:contactPoints\", \"cleaned_label\": \"contact points\", \"description\": \"A contact point for a person or organization.\", \"type\": \"rdf:Property\", \"domain\": [\"schema:Organization\", \"schema:Person\"], \"range\": [\"schema:ContactPoint\"], \"superclasses\": null, \"superproperties\": null}, \"Comments\": {\"id\": \"schema:comment\", \"cleaned_label\": \"comment\", \"description\": \"Comments, typically from users.\", \"type\": \"rdf:Property\", \"domain\": [\"schema:RsvpAction\", \"schema:CreativeWork\"], \"range\": [\"schema:Comment\"], \"superclasses\": null, \"superproperties\": null}, \"Author\": {\"id\": \"schema:author\", \"cleaned_label\": \"author\", \"description\": \"The author of this content or rating. Please note that author is special in that HTML 5 provides a special mechanism for indicating authorship via the rel tag. That is equivalent to this and may be used interchangeably.\", \"type\": \"rdf:Property\", \"domain\": [\"schema:CreativeWork\", \"schema:Rating\"], \"range\": [\"schema:Person\", \"schema:Organization\"], \"superclasses\": null, \"superproperties\": null}, \"Title\": {\"id\": \"schema:title\", \"cleaned_label\": \"title\", \"description\": \"The title of the job.\", \"type\": \"rdf:Property\", \"domain\": [\"schema:JobPosting\"], \"range\": [\"schema:Text\"], \"superclasses\": null, \"superproperties\": null}, \"URL\": {\"id\": \"schema:URL\", \"cleaned_label\": \"url\", \"description\": \"Data type: URL.\", \"type\": \"rdfs:Class\", \"domain\": null, \"range\": null, \"superclasses\": [\"schema:Text\"], \"superproperties\": null}, \"Content\": {\"id\": \"schema:WebContent\", \"cleaned_label\": \"web content\", \"description\": \"WebContent is a type representing all [[WebPage]], [[WebSite]] and [[WebPageElement]] content. It is sometimes the case that detailed distinctions between Web pages, sites and their parts is not always important or obvious. The  [[WebContent]] type makes it easier to describe Web-addressable content without requiring such distinctions to always be stated. (The intent is that the existing types [[WebPage]], [[WebSite]] and [[WebPageElement]] will eventually be declared as subtypes of [[WebContent]]).\", \"type\": \"rdfs:Class\", \"domain\": null, \"range\": null, \"superclasses\": [\"schema:CreativeWork\"], \"superproperties\": null}, \"Created\": {\"id\": \"schema:locationCreated\", \"cleaned_label\": \"location created\", \"description\": \"The location where the CreativeWork was created, which may not be the same as the location depicted in the CreativeWork.\", \"type\": \"rdf:Property\", \"domain\": [\"schema:CreativeWork\"], \"range\": [\"schema:Place\"], \"superclasses\": null, \"superproperties\": null}
                }, 
            \"schema_semantic_similarities\": 
                {
                    \"ID\": 1.0, 
                    \"Type\": 0.8027, 
                    \"Story\": 0.8327, 
                    \"Parent\": 1.0, 
                    \"Points\": 0.75, 
                    \"Comments\": 0.792, 
                    \"Author\": 1.0, 
                    \"Title\": 1.0, 
                    \"URL\": 1.0, 
                    \"Content\": 0.8487, 
                    \"Created\": 0.7486
                }, 
            \"table_domain\": 
                {
                    \"schema_syntactic\": \"schema:Rating\", 
                    \"schema_semantic\": \"schema:CreativeWork\", 
                    \"dbpedia_syntactic\": \"http://dbpedia.org/ontology/Person\", 
                    \"dbpedia_semantic\": \"http://dbpedia.org/ontology/Person\"
                }, 
            \"anonymized_columns\": [],
            \"table_id\": 7062
        }",
    "pandas": 
        "{
            \"index_columns\": 
                [
                    {
                        \"kind\": \"range\", 
                        \"name\": null, 
                        \"start\": 0, 
                        \"stop\": 10, 
                        \"step\": 1
                    }
                ], 
            \"column_indexes\": 
                [
                    {
                        \"name\": null, 
                        \"field_name\": null, 
                        \"pandas_type\": \"unicode\", 
                        \"numpy_type\": \"object\", 
                        \"metadata\": 
                            {
                                \"encoding\": \"UTF-8\"
                            }
                    }
                ], 
            \"columns\": 
                [
                    {
                        \"name\": \"ID\", 
                        \"field_name\": \"ID\", 
                        \"pandas_type\": \"int64\", 
                        \"numpy_type\": \"int64\", 
                        \"metadata\": null
                    }, 
                    {
                        \"name\": \"Type\", 
                        \"field_name\": \"Type\", 
                        \"pandas_type\": \"unicode\", 
                        \"numpy_type\": \"object\", 
                        \"metadata\": null
                    }, 
                    {
                        \"name\": \"Story\", 
                        \"field_name\": \"Story\", 
                        \"pandas_type\": \"float64\", 
                        \"numpy_type\": \"float64\", 
                        \"metadata\": null
                    }, 
                    {
                        \"name\": \"Parent\", 
                        \"field_name\": \"Parent\", 
                        \"pandas_type\": \"float64\", 
                        \"numpy_type\": \"float64\", 
                        \"metadata\": null
                    }, 
                    {
                        \"name\": \"Points\", 
                        \"field_name\": \"Points\", 
                        \"pandas_type\": \"int64\", 
                        \"numpy_type\": \"int64\", 
                        \"metadata\": null
                    }, 
                    {
                        \"name\": \"Comments\",
                        \"field_name\": \"Comments\", 
                        \"pandas_type\": \"int64\", 
                        \"numpy_type\": \"int64\", 
                        \"metadata\": null
                    }, 
                    {
                        \"name\": \"Author\", 
                        \"field_name\": \"Author\", 
                        \"pandas_type\": \"unicode\", 
                        \"numpy_type\": \"object\", 
                        \"metadata\": null
                    }, 
                    {
                        \"name\": \"Title\", 
                        \"field_name\": \"Title\", 
                        \"pandas_type\": \"unicode\", 
                        \"numpy_type\": \"object\",
                        \"metadata\": null
                    },
                    {
                        \"name\": \"URL\", 
                        \"field_name\": \"URL\", 
                        \"pandas_type\": \"unicode\", 
                        \"numpy_type\": \"object\", 
                        \"metadata\": null
                    }, 
                    {
                        \"name\": \"Content\", 
                        \"field_name\": \"Content\", 
                        \"pandas_type\": \"unicode\", \
                        "numpy_type\": \"object\", 
                        \"metadata\": null}, 
                    {
                        \"name\": \"Created\", 
                        \"field_name\": \"Created\", 
                        \"pandas_type\": \"int64\", 
                        \"numpy_type\": \"int64\", 
                        \"metadata\": null
                    }
                ], 
            \"creator\": 
                {
                    \"library\": \"pyarrow\", 
                    \"version\": \"4.0.0\"}, 
                    \"pandas_version\": \"1.4.1\"
                }"
}
```
### table
在本例子中整理为table.csv

与GitTables_1M_csv中的原表内容相同：
|    ID  |  Type   |   Story   |  Parent  | Points | Comments |  Author   |           Title           |                                   URL                                   | Content |   Created   |
|--------|---------|-----------|----------|--------|----------|-----------|---------------------------|-------------------------------------------------------------------------|---------|-------------|
|  34644 | comment |  34461.0  | 34461.0  |   0    |    0     |  herdrick |                           |                                                                         |         | 1184633825  |
|  34643 | comment |  34461.0  | 34640.0  |   0    |    0     | euccastro |                           |                                                                         |         | 1184632694  |
|  34642 | comment |  34461.0  | 34629.0  |   0    |    0     |   mdakin  |                           |                                                                         |         | 1184632537  |
|  34641 |  story  |           |          |   3    |    0     |   nickb   | The man who saddled...    | [http://valleywag.com/tech/don.t-be-evil/the-man-who-saddled-google...] |         | 1184632512  |
|  34640 | comment |  34461.0  | 34634.0  |   0    |    0     | mattculbreth |                       |                                                                         |         | 1184631964  |
|  34639 |  story  |           |          |   11   |    5     | horatio05 | Get Yourself A Morning...| [http://www.codesqueeze.com/get-yourself-a-morning-ritual/]            |         | 1184631874  |
|  34638 | comment |  34542.0  | 34593.0  |   0    |    0     |   gleb    |                           |                                                                         |         | 1184631763  |
|  34637 |  story  |           |          |   4    |    5     | horatio05 | 101 Ways To Know Your... | [http://www.codesqueeze.com/101-ways-to-know-your-software-project...] |         | 1184631326  |
|  34636 | comment |  34454.0  | 34454.0  |   0    |    0     | jamesbritt |                           |                                                                         |         | 1184631263  |
|  34635 | comment |  34461.0  | 34569.0  |   0    |    0     | euccastro |                           |                                                                         |         | 1184630808  |
