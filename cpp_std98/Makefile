NAME := project_name_here

CC := c++
CFLAGS := -Wall -Werror -Wextra -std=c++98 -I utils/

SRCSDIR := srcs/
OBJSDIR := objs/

SRCS := main.cpp

OBJS := $(SRCS:%.cpp=$(OBJSDIR)%.o)

all:
	make $(NAME)

$(NAME): $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@

$(OBJSDIR)%.o: $(SRCSDIR)%.cpp
	mkdir -p $(OBJSDIR)
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -rf $(OBJSDIR) 

fclean: clean
	rm -rf $(NAME)

re: fclean
	make $(NAME)

.PHONY: all clean re fclean
