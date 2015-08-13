## NAME
python data structures list serialized and deserialization

## SYNOPSIS
    from DataStructuresSerialized import DataStructuresSerialized

    city       = ["China", "010", "beijing"]
    separator  = '|'
    serialized = DataStructuresSerialized(city, separator).getSerializedString()
    print(serialized)

    _DataStructuresSerialized $_ China|010|beijing

    cityString = "China|010|beijing"
    separator  = '|'
    city       = DataStructuresSerialized(city, separator).getDeserializationStruct()
    print(city)

    _DataStructuresSerialized $_ ['China', '10', 'beijing']

    cityString = "China|010|beijing"
    separator  = '|'
    index      = 1
    newString  = "000"
    city       = DataStructuresSerialized(cityString, separator)
    
    city.update(index, newString)
    newCityString = city.getSerializedString()
    
    print(newCityString)

    _DataStructuresSerialized $_ China|000|beijing

## DESCRIPTION
#### getSerializedString
    return serialized string, only support list data structures serialized

#### getDeserializationStruct
    return deserialization list data struct

#### update
    update serialized string or list data structures some substring
