### 指针

``` c++
#include <iostream>
#define LOG(x) std::cout << x << std::endl;
int main()
{
	// equal void* ptr = nullptr; // equal void* ptr = NULL
	void* ptr = 0; 
	
	int var = 8;				// create a var in stack

	// types doesn't matter
	//void* ptr2 = &var;		// take the memory address of var
	int* ptr2 = &var;			
	//double* ptr2 = (double*)&var;

	*ptr2 = 10; // derefence
	LOG(var);

	// create data on heap, should delete after using
	char* buffer = new char[8];
	memset(buffer, 0, 8);

	// pointers to pointers
	char** ptr3 = &buffer;

	delete[] buffer;

	// pointers are also variables
	
	std::cin.get();
}

```

<img width="1265" height="606" alt="Image" src="https://github.com/user-attachments/assets/1cc6bee7-9c76-430d-9ac3-f1145368e566" />

<img width="962" height="967" alt="Image" src="https://github.com/user-attachments/assets/9d0a62e5-0107-432b-90fb-c607d6befe7c" />