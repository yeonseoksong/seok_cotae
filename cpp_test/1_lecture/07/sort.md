- 정렬과 탐색
	1. 기본적인 정렬 알고리즘
		- 정렬(sort)
			- 주어진 데이터를 정해진 기준에 따라 순서를 재배열하는 직업
			- 가장 기본적이고 중요한 알고리즘 중의 하나
				- 입력 데이터 : 4 2 3 5 1
				- 오름차순(ascending order) : 1 2 3 4 5
				- 내림차순(descending order) : 5 4 3 2 1

		- 다양한 정렬 알고리즘
			- 단순하고 비효율적
				- 버블 정렬
				- 선택 정렬
				- 삽입 정렬
			- 복잡하고 효율적
				- 쉘 정렬
				- 병합 정렬
				- 퀵 정렬
				- 힙 정렬
				- 기수 정렬
		
		- 정렬 알고리즘의 평가 척도
			- 비교횟수 & 이동횟수
			- 모든 경우에 최적인 정렬 알고리즘은 없다. 따라서 응용에 맞게 선택해야 한다.

		- 정렬 알고리즘의 안정성
			- 안정된(stable) 정렬 : 같은 값을 갖는 원소의 순서가 정렬 후에도 유지된다.
			- 안정되지 않은 정렬 : 같은 값을 갖는 원소의 순서가 정렬 후에 보장되지 않는다.
			- 예시 : (Kim, 34) (Lee, 30) (Choi, 25) (Park, 30)
				- 나이순으로 오름차순을 정렬한다면?
				- stable : (Choi, 25) (Lee, 30) (Park, 30) (Kim, 34)
				- unstable : (Choi, 25) (Park, 30) (Lee, 30) (Kim, 34)
		
		- 버블 정렬(bubble sort)
			- 정렬되지 않은 부분에서 인접한 두 원소의 크기를 비교하여 교환하는 작업을 반복
			- data[n-1]부터 data[i]까지 이동하면서 인접한 두 원소를 비교 및 교환
			- for 반복문 내부 문장의 실행 횟수 : O(n^2)
		
		- 선택 정렬(selection sort)
			- 정렬되지 않은 원소들 중에서 최소값 원소를 찾아 맨 왼쪽 원소와 교환
			- data[i], data[i+1], ..., data[n-1]에 대해 최솟값을 갖는 인텍스(idx)를 알아낸 후, data[i]와 data[idx]를 교환한다.
			- 시간 복잡도 : O(n^2)

		- 삽입 정렬(insertion sort)
			- 정렬되지 않은 부분의 첫 번째 원소를 정렬된 부분의 알맞은 위치에 삽입하는 과정을 반복한다.
			- data[i]를 임시 변수(key)에 복사한 후, data[i-1]부터 data[0]까지 차례로 검사하면서 key를 삽입하기에 적절한 위치를 찾을 때까지 각각의 원소 값을 오른쪽 원소로 복사하고, 적절한 위치에 key 값을 삽입(복사)

			- 시간 복잡도
				- 최선의 경우 : O(n - 1)
				- 최악의 경우 : O(n^2)
	2. 분할 정복과 정렬 알고리즘
        - 분할 정복(divide and conquer)
			- 주어진 문제의 규모가 커거 한 번에 해결하기 어려운 경우, 이를 작은 부분 문제로 나눠서 해결하는 방식

			- 분할(divide) : 주어진 문제를 동일한 방식으로 해결할 수 있는 부분 문제로 나누기
			- 정복(conquer) : 각 부분 문제에 대한 솔루션 구하기
			- 결합(combine) : 각 부분 문제의 솔루션을 결합하여 전체 문제에 대한 솔루션 구하기

		- 분할 정복을 이용한 정렬 알고리즘
			- 병합 정렬(merge sort)
			- 퀵 정렬(quick sort)
			- 힙 정렬(heap sort)

			- 병합 정렬 (Merge sort)
				- 분할 정복에 의한 정렬 알고리즘의 하나
				- 입력 배열을 두 개의 부분 배열로 분할
				- 부분 배열을 재귀적으로 정렬
				- 부분 배열을 병합
					- 이때, 병합된 배열의 원소가 정해진 정렬 순서에 부합되도록 순서를 조정
				- 병합 정렬의 시간 복잡도
					- 배열을 분할 또는 병합하는 단계 : log n
					- 배열 병합하는 과정의 시간 복잡도 : O(n)
					- 전체 시간 복잡도 : O(n log n)

				- 병합 정렬의 특징
					- 실제 정렬이 이루어지는 시점은 두 개의 부분 배열이 병합하는 단계
					- 안정된 정렬, 데이터의 추기 순서에 영향을 크게 받지 않음
					- 병합 과정에서 임시 배열을 필요로 함 (공간 복잡도 : O(n))

			- 퀵 정렬(quick sort)
				- 병합 정렬과 마찬가지로 분할 정복에 의한 정렬 알고리즘
				- 특정 원소를 피벗(pivot)으로 선택하고, 주어진 배열을 피벗보다 작은 부분과 큰 부분으로 분할
					- 피벗 : 비교 기준 원소
				- 분할된 부분 배열에 대해 재귀적으로 퀵 정렬 분할 작업을 반복

				- 퀵 정렬의 시간 복잡도
					- 최선의 경우 : O(n log n) (항상 절반으로 분할되는 경우)
					- 최악의 경우 : O(n^2) (한 쪽은 1개, 다른 쪽은 n-1개로 분할되는 경우)
					- 퀵 정렬과 병합 정렬의 시간 복잡도

						| 알고리즘 | 최선 | 평균 | 최악 |
						|:----:|:----:|:----:|:----:|
						|병합 정렬|```O(n log n)```|```O(n log n)```|```O(n log n)```|
						|퀵 정렬|```O(n log n)```|```O(n log n)```|```O(n^2)```|
				
				- 튁 정렬의 특징
					- 실제 정렬이 이루어지는 시점은 배열을 피벗 기준으로 분할하는 단계임
					- 안정되지 않은 정렬이며, 데이터의 초기 순서의 영향을 크게 받음
					- 평균적으로 가장 빠른 정렬 알고리즘
						- C/C++ 라이브러리로 기본 제공되는 정렬 알고리즘
	3. ```std::sort()``` 함수 사용하기
		- ```std::sort()``` 함수
			
			```C++
			template <class RandomIt>
			void sort(RandomIt first, RandomIt last);

			template <class RandomIt, class Compare>
			void sort(RandomIt first, RandomIt last, Compare comp);
			```

			- 순차 컨테이너에 대해 ```[first, last)``` 범위의 원소들을 정해진 방법으로 정렬 (기본값 : 오름차순)
			- 같은 값을 갖는 원소의 순서는 보장되지 않음 (순서를 유지하려면 ```std::stable_sort()``` 함수 사용)
			- ```std::sort()``` 함수는 ```O(n log n)```으로 동작해야 하며, 실제 구현은 컴파일러에 따라 다를 수 있다.
			- C 스타일 배열, vector, deque, array를 정렬 할 때 주로 사용
				- list, forward_list는 자체 멤버 함수 사용
			- ```comp``` 인자에 비교 함수 객체를 전달할 수 있다.
			- ```<algorithm>```에 정의되어 있음
	4. 선형 탐색과 이진 탐색
		- 선형 탐색(linear search)
			- 전체 자료를 처음부터 마지막까지 순서대로 탐색하는 방법
			- 순차 탐색
			- 시간 복잡도 : O(n)
		- 선형 탐색의 장단점
			- 장점 : 가장 간단하고 직관적인 방법이며, 정렬되지 않은 데이터에도 적용 가능
			- 단점 : 비효율적 (최악의 경우 배열 전체를 탐색해야 함)

		- 이진 탐색(binary search)
			- 정렬된 배열에 대해 검색 단계별로 검색 범위를 반으로 줄여가면서 데이터를 탐색하는 기법
			- 시간 복잡도 : O(log n)

		- 이진 탐색의 장단점
			- 장점 : 검색 속도가 빠름
			- 단점 : 이미 정렬되어 있는 데이터에만 적용 가능
	
		- ```std::binary_search()``` 함수
			
			```C++
            template <class ForwardIt, class T>
			bool binary_search(ForwardIt first, ForwardIt last, const T& value);

			template <class ForwardIt, class T, class Compare>
			bool binary_search(ForwardIt first, ForwardIt last, const T& value, Compare comp);
			```

			- 정렬된 컨테이너에서 ```[first, last)``` 범위 안에 value 값이 있는지를 검사
			- 최소 ```[first, last)``` 범위 안에서라도 정렬이 되어 있어야 동작
			- 기본적으로 ```<``` 연산자를 이용하여 값을 비교하고, 비교 함수 ```comp```를 지정할 수도 있다.
			- ```<algorithm>```에 정의되어 있음