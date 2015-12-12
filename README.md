# c2vector
Vector implementation in C2. Based on vector implementation
in C by Edd Mann

## API
```
public type vector struct
{
    void** items;
    int32 capacity;
    int32 total;
}

public func void init(vector* v);
public func int32 total(vector* v);
public func void add(vector* v, void* item);
public func void set(vector* v, int32 index, void* item);
public func void* get(vector* v, int32 index);
public func void delete(vector* v, int32 index);
public func void free(vector *v);
```
## Usage

Always start by declaring and initializing a vector (import c2vector local; and import stdio as io; assumed)
```
vector vc;
init(&vc);
```
Then you can add any kind of item to the vector with
```
add(&vc, item);
```
Get item at any position
```
get(&vc, 1);
```
The total function returns the number of elements in a vector.
```
io.printf("%d\n, total(&vc));
```
After you are done working with a vector, you can free it with
```
free(&vc);
```

## License