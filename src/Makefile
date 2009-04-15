CC      = gcc
PROF    = 

C_FLAGS = -O -g3 -Wall -DACK $(PROF)
L_FLAGS = -O -g3 $(PROF) -lcrypt

O_FILES = act_comm.o act_info.o act_move.o act_obj.o act_wiz.o comm.o const.o \
          db.o fight.o handler.o interp.o magic.o magic2.o mob_commands.o mob_prog.o   \
	  save.o special.o update.o board.o areasave.o buildtab.o build.o     \
          write.o act_clan.o buildare.o hunt.o hash.o areachk.o clutch.o      \
          obj_fun.o act_mob.o macros.o trigger.o magic3.o quest.o lists.o  \
          social-edit.o vampyre.o werewolf.o \
          mount.o pdelete.o wizutil.o ssm.o scheck.o rulers.o spendqp.o enchant.o


merc: $(O_FILES)
	rm -f merc
	$(CC) -o merc $(O_FILES) $(L_FLAGS)

.c.o: merc.h
	$(CC) -c $(C_FLAGS) $<

scan: scan.o
	rm -f scan
	$(CC) -o scan scan.o $(L_FLAGS)

clean:
	rm -f $(O_FILES) merc ../area/core
	make

purge:
	rm $(O_FILES) merc
