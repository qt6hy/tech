
# c++ singleton example

```cpp

class Foo {

private:
    Foo();
    ~Foo();

public:
    // これは無くてもいい ===>>>
    Foo(const Foo&) = delete;
    Foo& operator=(const Foo&) = delete;
    Foo(Foo&&) = delete;
    Foo& operator=(Foo&&) = delete;
    // これは無くてもいい ===<<<

    static Foo& get_instance() {
        static Foo instance;
        return instance;
    }
};
```
