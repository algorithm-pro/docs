示例：
int k=3;
int[] arr = [4,5,8,2];


利用优先队列来实现：
```
class KthLargest {
	final PriorityQueue<Integer> q;
	final int k;
	public HthLargest(int k, int[] a) {
		this.k = k;
		q = new PriorityQueue<>(k);
		for (int n: a)
			add(n)
	}
	public int add(int n){
		if (q.size() < k)
			q.offer(n);
		else if (q.peek()<n){
			q.poll();
			q.offer(n);
		}
	}
	return q.peek();
}
```
