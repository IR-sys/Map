# Map
To implement map
#include<iostream>
#include<map>
#include<string>
#include<utility>
using namespace std;
int main(){
	typedef map<string,int>mapType;
	mapType populationMap;
	
	populationMap.insert(pair<string,float>("Maharashtra",125));
	populationMap.insert(pair<string,float>("uttar pradesh",225));
	populationMap.insert(mapType::value_type("Bihar",120));
	populationMap.insert(mapType::value_type("West bengal",100));
	populationMap.insert(make_pair("punjab",31));
	populationMap.insert(make_pair("gujarat",70));
	populationMap.insert(make_pair("haryana",29));
	populationMap.insert(make_pair("uttarakand",12));
	populationMap.insert(make_pair("telengana",37));
	populationMap.insert(make_pair("Madhya pradesh",90));
	populationMap.insert(make_pair("andra pradesh",53));
	populationMap.insert(make_pair("jharkand",38));
	populationMap.insert(make_pair("karnataka",68));
	populationMap.insert(make_pair("odisha",47));
	populationMap.insert(make_pair("rajasthan",78));
	populationMap.insert(make_pair("kerala",38));
	populationMap.insert(make_pair("tamil nadu",80));
	populationMap.insert(make_pair("goa",2));
	populationMap.insert(make_pair("chattisgarh",30));
	populationMap.insert(make_pair("tripura",4));
	populationMap.insert(make_pair("assam",35));
	populationMap.insert(make_pair("nagaland",2));
	populationMap.insert(make_pair("arunachal pradesh",2));
	populationMap.insert(make_pair("meghalaya",4));
	populationMap.insert(make_pair("mizoram",1));
	populationMap.insert(make_pair("manipur",3));
	populationMap.insert(make_pair("sikkim",1));
	populationMap.insert(make_pair("UT adaman and nicobar",1));
	populationMap.insert(make_pair("UT Delhi",19));
	populationMap.insert(make_pair("UT chandigarh",1));
	populationMap.insert(make_pair("UT Dadara nagar and haveli daman and diu",1));
	populationMap.insert(make_pair("UT Lakshdeep",0000.3));
	populationMap.insert(make_pair("UT Ladakh",000.6));
	populationMap.insert(make_pair("UT jammu and kashmir",14));
	populationMap.insert(make_pair("UT Paducherry",2));
	
	mapType::iterator iter=--populationMap.end();
	populationMap.erase(iter);
	
	cout<<"Total states and UT in the map:"<<populationMap.size()<<'\n';
	for(iter=populationMap.begin();iter!=populationMap.end();++iter){
		cout<<iter->first<<":"<<iter->second<<"million\n";
	}
	char c;
	do{
		string state;
		cout<<"Enter the state to know its population:";
		cin>>state;
		iter=populationMap.find(state);
		if(iter!=populationMap.end())
		cout<<state<<"s population is"<<iter->second<<"million\n";
		else
		cout<<"State is not found";
		cout<<"Do you want to continue(y/n):";
		cin>>c;
			}
			while(c=='y'||c=='Y');
			populationMap.clear();
			return 0;
	
	
}
