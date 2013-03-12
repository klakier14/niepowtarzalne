niepowtarzalne
==============

niepowtarzalne

  if (strcmp("/test", cmdtext, true, 10) == 0)
	{
			new spawnpos[3][5];
			spawnpos[0][0]=2626;
			spawnpos[1][0]=1227;
			spawnpos[2][0]=26;
			
			spawnpos[0][1]=2657;
			spawnpos[1][1]=1228;
			spawnpos[2][1]=26;
			
			spawnpos[0][2]=2662;
			spawnpos[1][2]=1195;
			spawnpos[2][2]=26;
			
			spawnpos[0][3]=2632;
			spawnpos[1][3]=1196;
			spawnpos[2][3]=26;
			
			spawnpos[0][4]=2647;
			spawnpos[1][4]=1211;
			spawnpos[2][4]=26;

			new rand,s;
			new randt[sizeof(spawnpos[])];
		//	new tekst[1024];
			for(new i=0; i<GetMaxPlayers(); i++)
			{
				do
				{
					s=1;
					rand = random(sizeof(spawnpos[]));
					for(new j=0;j<i;j++)
						if(rand==randt[j]) s=2;
				} while(s==2);
				randt[i] = rand;
			//	format(tekst,sizeof(tekst),"%d:%d",i,rand);
			//	SendClientMessage(playerid,NIEBIESKI,tekst);
				SetPlayerPos(i, spawnpos[0][rand], spawnpos[1][rand], spawnpos[2][rand]);
			}
			return 1;
	}
