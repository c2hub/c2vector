# c2vector
Vector implementation in C2. Based on vector implementation
in C by Edd Mann
After downloading or cloning c2vector, it is advised to test
it with
```
c2c --test
```
in the the root directory of the c2vector repository
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
Lukas Hozda(luk.hozda@gmail.com, github.com/luciusmagn), (c)2015

Usage of the works is permitted provided that this instrument is
retained with the works, so that any entity that uses the works
is notified of this instrument.								  

DISCLAIMER: THE WORKS ARE WITHOUT WARRANTY.						