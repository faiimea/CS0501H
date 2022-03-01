#include <iostream>
using namespace std;
struct node
{
	int ID;
	node* next;
	node* prio;
};
int main()
{
	int num,opnum;
	cin >> num>>opnum;
	node* head;
	head = new node;
	head->prio = NULL;
	head->next = NULL;
	node* m;
	m = head;
	int tmp;
	for (int i = 0;i < num;++i)
	{
		cin >> tmp;
		node* temp;
		temp = new node;
		temp->prio = m;
		temp->ID = tmp;
		m->next = temp;
		temp->next = NULL;
		m = m->next;
	}
	int State;
	int X, Y;
	int now;
	now = 0;
	m = head;
	for (int j = 0;j < opnum;++j)
	{
		cin >> State;
		if (State == 1)
		{
			cin >> X >> Y;
			if (X != 0)
			{
				while (X--)
				{
					m = m->next;
				}
			}
			else
			{
				m = head;
			}
			node* temp;
			temp = new node;
			temp->next = m->next;
			temp->prio = m;
			if (m->next != NULL) m->next->prio = temp;
			m->next = temp;
			temp->ID = Y;
		}
		else
		{
			cin >> X;
			while (X--)
			{
				m = m->next;
			}
				
			m->prio->next = m->next;
			if (m->next != NULL) m->next->prio = m->prio;					
		}
		m = head;
	}
	node* m1;
	m1 = head->next;
	while (m1 != NULL)
	{
		cout << m1->ID << ' ';
		m1 = m1->next;
	}
}
