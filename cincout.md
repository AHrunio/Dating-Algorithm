

## 一维数组输入

```cc
//空格分割
	//6
	//1 2 3 4 5 6
	int num;
	cin >> num;
	vector<int> nums;
	int temp_num;
	for (int i = 0; i < num; i++)
	{
		cin >> temp_num;
		nums.push_back(temp_num);
	}
	
	//逗号分割
	//5
	//1,2,3,4,5
	int num;
	cin >> num;
	vector<int> nums;
	int temp_num;
	for (int i = 0; i < num-1; i++)
	{
		char a;
		cin >> temp_num >>a;
		nums.push_back(temp_num);
	}
	cin >> temp_num;
	nums.push_back(temp_num);
```

## 二维数组输入

```cc
//2 3
	//56 78
	//23 45 12
	int m, n;
	cin >> m >> n;
	vector<vector<int>> p(m, vector<int>(n));
	for (int i = 0; i < m; i++)
		for (int j = 0; j < n; j++)
			cin >> p[i][j];
```

## 输入字符串，有空格

```cc
string str;
	// cin >> str;			输入 uuu ioi 输出 uuu
	//getline(cin, str);    输入 i love you 输出 i love you
	getline(cin, str);
```

## 以 ‘,’分割字符串输入

```cc
/*
	2
	67 89
	4
	12 34 56 78
	...
	*/
	vector<vector<int>> a;
	int n;
	while (cin >> n) {    //遇到文件结束符停止,windods命令行输入文件结束符，ctrl+z然后enter
		vector<int> b(n,0);
		for (int i = 0;i < n;i++)
			cin >> b[i];
		a.push_back(b);
	}
```

## 一行数据不确定多少，但是以enter结尾

```cc
//1 2 3 4 5...
	//8 9 6...
	int m, n;
	vector<int>a, b;
	while (cin >> m) {
		a.push_back(m);
		if (cin.get() == '\n') break;
	}
	while (cin >> n) {
		b.push_back(n);
		if (cin.get() == '\n') break;
	}
```

一行 n个string，每个string空格隔开，一共三行

```cc
/*
hello ,
i am a coder
hello , i am a singer
*/
	set<string> stop;
	string tem;
	while (cin >>tem) {
		stop.insert(tem);
		if (cin.get() == '\n') break;
	}

	vector<string> A;
	while (cin >> tem) {
		if(stop.count(tem)==0) //过滤停用词
			A.push_back(tem);
		if (cin.get() == '\n') 
			break;
	}
	vector<string> B;
	while (cin >> tem) {
		if (stop.count(tem) == 0) //过滤停用词
			B.push_back(tem);
		if (cin.get() == '\n')
			break;
	}
```

