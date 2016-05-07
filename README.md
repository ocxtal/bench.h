# bench.h

Benchmarking utility. include `bench.h`, declare `bench_t` variable, use `bench_init`, `bench_start`, `bench_end` and `bench_get`.

## Example

```
#include <stdio.h>
#include "bench.h"

int main(void)
{
	bench_t v;
	bench_init(v);

	/* task 1 */
	bench_start(v);
	
	/* do something heavy... */
	
	bench_end(v);

	/* task 2 */
	bench_start(v);
	
	/* do another... */
	
	bench_end(v);


	printf("total: %lld us\n", bench_get(s));
	return(0);
}
```

## License

MIT