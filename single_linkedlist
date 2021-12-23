#include<stdio.h>
#include<malloc.h>
#include<stdlib.h>

struct node
{
	int data;
	struct node *next;
}*start;

create_list()
{
	int data;
	struct node *q,*tmp;
	tmp=malloc(sizeof(struct node));
	q=malloc(sizeof(struct node));
	printf("Enter the data: ");
	scanf("%d",&tmp->data);
	tmp->next=NULL;
	if(start==NULL)
		start=tmp;
	else
	{
		q=start;
		while(q->next!=NULL)
		{
			q=q->next;
		}
		q->next=tmp;
	}
}

display()
{
	struct node *q;
	q=malloc(sizeof(struct node));
	if(start==NULL)
	{
		printf("List is empty");
		return;
	}
	q=start;
	printf("List is:\n");
	while(q!=NULL)
	{
		printf(" %d ", q->data);
		q=q->next;
	}
	printf("\n");
}

insert_beg()
{
	int data;
	struct node *tmp;
	tmp=malloc(sizeof(struct node));
	printf("Enter the data: ");
	scanf("%d",&data);
	tmp->next=start;
	start=tmp;
}

insert_mid()
{
	int data,pos,i;
	struct node *q,*tmp;
	tmp=malloc(sizeof(struct node));
	q=malloc(sizeof(struct node));
	q=start;
	printf("Enter the position: ");
	scanf("%d",&pos);
	printf("Enter the data: ");
	scanf("%d",&data);
	for(i=1;i<pos-1;i++)
	{
		q=q->next;
		if(q==NULL)
		{
			printf("There are less then %d elements in the list",pos);
			return;
		}
	}
	tmp->data=data;
	tmp->next=q->next;
	q->next=tmp;
}

insert_end()
{
	int data;
	struct node *q,*tmp;
	tmp=malloc(sizeof(struct node));
	q=malloc(sizeof(struct node));
	q=start;
	printf("Enter the data: ");
	scanf("%d",&data);
	tmp->data=data;
	tmp->next=NULL;
	while(q->next!=NULL)
	{
		q=q->next;
	}
	q->next=tmp;
}

delete_beg()
{
	struct node *tmp;
	tmp=malloc(sizeof(struct node));
	tmp=start;
	start=tmp->next;
	free(tmp);
}

delete_mid()
{
	int pos,i;
	struct node *q,*tmp;
	tmp=malloc(sizeof(struct node));
	q=malloc(sizeof(struct node));
	q=start;
	printf("Enter the position: ");
	scanf("%d",&pos);
	for(i=1;i<pos-1;i++)
	{
		q=q->next;
		if(q=NULL)
		{
			printf("There are less then %d elements in the list",pos);
			return;
		}
	}
	tmp=q->next;
	q->next=tmp->next;
	free(tmp);
}

delete_end()
{
	struct node *tmp,*q;
	tmp=malloc(sizeof(struct node));
	q=malloc(sizeof(struct node));
	q=start;
	while(q->next->next!=NULL)
	{
		q=q->next;
	}
	tmp=q->next;
	q->next=NULL;
	free(tmp);
}

count()
{
	int count=0;
	struct node *q;
	q=malloc(sizeof(struct node));
	q=start;
	while(q!=NULL)
	{
		q=q->next;
		count++;
	}
	printf("Total no. of node: %d", count);
	printf("\n");
}

search()
{
	 int item,pos=1;
	 struct node *q;
	 q=malloc(sizeof(struct node));
	 q=start;
	 printf("Enter the item you want to search: ");
	 scanf("%d",&item);
	 while(q!=NULL)
	 {
	 	if(q->data==item)
	 	{
	 		printf("%d found at position %d",item,pos);
	 		return;
	 	}
	 	q=q->next;
	 	pos++;
	 }
	 if(q==NULL)
	 printf("Item not found");
	 printf("\n");
}

main()
{
	int choice,n,m,pos,i;
	start=NULL;
	while(1)
	{
		printf("\n");
		printf("\tMENU\n");
		printf("1.  Create list\n");
		printf("2.  Display\n");
		printf("3.  Insert at the beginning\n");
		printf("4.  Insert at the middle\n");
		printf("5.  Insert at the end\n");
		printf("6.  Delete at the beginning\n");
		printf("7.  Delete at the middle\n");
		printf("8.  Delete at the end\n");
		printf("9.  Count the no. of elements\n");
		printf("10. Search items\n");
		printf("11. Quit\n");
		printf("Your choice: ");
		scanf("%d",&choice);
		printf("\n");
		switch(choice)
		{
			case 1:
				printf("How many nodes: ");
				scanf("%d",&n);
				for(i=0;i<n;i++)
				{
					create_list();
				}
				break;
			case 2:
				display();
				break;
			case 3:
				insert_beg();
				break;
			case 4:
				insert_mid();
				break;
			case 5:
				insert_end();
				break;
			case 6:
				delete_beg();
				break;
			case 7:
				delete_mid();
				break;
			case 8:
				delete_end();
				break;
			case 9:
				count();
				break;
			case 10:
				search();
				break;
			case 11:
				exit(1);
				break;
			default:
				printf("Please enter a valid choice");
		}
	}
}
