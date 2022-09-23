#include <bits/stdc++.h>
#include<ext/pb_ds/tree_policy.hpp>
#include<ext/pb_ds/assoc_container.hpp>
#include<ext/rope>
using namespace std;
using namespace __gnu_pbds;
using namespace __gnu_cxx;
template<class T> using policy_tree = tree<T, null_type, less<T>, rb_tree_tag,tree_order_statistics_node_update>;

using namespace std;
#define go ios::sync_with_stdio(0);cin.tie(nullptr);cout.tie(nullptr);
#define ll long long
const int mxn = 6e6 + 5 , mod = 1e9 + 7 , MOD = 1e9 + 7 , mod2 = 998244353;

struct Node{
	int data;
	Node* nxt;
};

struct LinkedList{
	Node* head = NULL;
	Node* tail = NULL;
	void insertBefore(int value){
		Node* new_node = new Node;
		new_node->data = value;
		new_node->nxt = NULL;
		if(head == NULL){
			head = new_node;
			tail = new_node;
		}else{
			new_node->nxt = head;
			head = new_node;
		}
	}
	void insertAfter(int value){
		Node* new_node = new Node;
		new_node->data = value;
		new_node->nxt = NULL;
		if(head == NULL){
			head = new_node;
			tail = new_node;
		}else{
			tail->nxt = new_node;
			tail = new_node;
		}
	}
	void display(){
		if(head == NULL){
			return void(cout<<"Linked List is Empty"<<endl);
		}else{
			Node* lst = head;
			while(lst != NULL){
				cout<<lst->data<<endl;
				lst = lst->nxt;
			}
		}
	}
	void Delete(int value){
		if(head == NULL){
			return void(cout<<"value not found"<<endl);
		}
		if(head->data == value){
			Node* del = head;
			head = head->nxt;
			free(del);
			return void(cout<<"Deleted .."<<endl);
		}
		Node* prv = head;
		Node* curr = head;
		while(curr != NULL){
			curr = curr->nxt;
			if(curr != NULL && curr->data == value){
				prv->nxt = curr->nxt;
				curr->nxt = NULL;
				free(curr);
				return void(cout<<"Deleted .."<<endl);
			}
			prv = prv->nxt;
		}
		return void(cout<<"value not found"<<endl);
	}
};

void bingo(){
	LinkedList L1 ;
	int q;
	cin>>q;
	while(q--){
		int st;
		cin>>st;
		if(st == 1)
			L1.display();
		else {
			int value;
			cin>>value;
			if(st == 2){
				L1.insertAfter(value);
			}else if(st == 3){
				L1.insertBefore(value);		
			}else{
				L1.Delete(value);
			}
		}
	}
}
int main() {
	go

//	freopen("flight.in", "rt", stdin);
//	freopen("flight.out", "wt", stdout);
	int t = 1;
	//cin>>t;
	while(t--){
		bingo();
	}
	return 0;
}
