
# VC++ Exception

```c++
try
{
  int a = 0;

  // 「はい (/EHsc)」：これは例外をスローしません
  // 「はい (/EHa)」：C++ 例外で捕捉できます
  int b = 1 / a;
  a = b;
}
catch (...)
{
     // エラーログ出力
}
```
