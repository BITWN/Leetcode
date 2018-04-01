## 360 笔试编程题 ##

----------
1.画板


     #include<iostream>
    using namespace std;
    int main()
    {
    	int num;
    	cin>>num;
    	while(num!=0)
    	{	int row;
    		cin>>row;
    		int sum=0;
    		while(row!=0)
    		{
    			int x1,x2,y1,y2;
    			cin>>x1>>y1>>x2>>y2;
    		//	cout<<"x2-x1:"<<x2-x1<<"  y2-y1:"<<y2-y1<<endl;
    			sum=sum+(x2-x1+1)*(y2-y1+1);
    			row--;
    		//	cout<<"row:"<<row<<endl;
    		}
    		cout<<sum;
    		num--;
    	}
    }
    

----------
2.派对

    #include<iostream>
    #include<algorithm>
    #include<vector>
    using namespace std;
    int main()
    {
    	int n;
    	cin>>n;
    	vector<int>v;
    	int r,g,b;
    	for(int i=0;i<n;i++)
    	{
    		cin>>r>>g>>b;
    		v.push_back(r);
    		v.push_back(g);
    		v.push_back(b);
    		sort(v.begin(),v.end());
    		r=r-v[0];
    		g=g-v[0];
    		b=b-v[0];
    		if(r+g+b>=3)
    		{
    			cout<<v[0]+(r+g+b)/3;
    		}
    		else
    		{
    			cout<<v[0];
    		}
    	}
    	return 0;
    }
