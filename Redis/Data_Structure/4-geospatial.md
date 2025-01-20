# [Geospatial](https://redis.io/docs/latest/develop/data-types/geospatial/)

Redis Geospatial is a specialized data type that allows you to store, query, and manipulate geospatial data such as coordinates (latitude and longitude). It is ideal for use cases like location-based services, maps, or proximity searches.

## Key Features
- Store geospatial points (latitude, longitude, and a name).
- Query for nearby points or points within a given radius.
- Retrieve distances between points.
- Works efficiently with geohashes internally for fast queries.

---

## Commands

### Adding Geospatial Data
- **GEOADD `<key>` `<longitude>` `<latitude>` `<member>`**: Adds a geospatial point (longitude, latitude) with a name (`member`) to the specified key.

```shell
# Example Commands
geoadd locations 77.5946 12.9716 "Bangalore"
geoadd locations 72.8777 19.0760 "Mumbai"
geoadd locations 88.3639 22.5726 "Kolkata"