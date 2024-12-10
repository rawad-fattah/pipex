PROG	= pipex

SRCS 	= srcs/pipex.c srcs/utils.c
OBJS 	= ${SRCS:.c=.o}

HEADER	= -Iincludes

CC 		= gcc
CFLAGS 	= -Wall -Wextra -Werror

%.o: %.c
	${CC} ${CFLAGS} ${HEADER} -c $< -o $@

all: ${PROG}

${PROG}: ${OBJS}
	@make re -C ./libft
	${CC} ${OBJS} -Llibft -lft -o ${PROG}

clean:
	@make clean -C ./libft
	rm -f ${OBJS}

fclean: clean
	@make fclean -C ./libft
	rm -f ${PROG}

re: fclean all

.PHONY: all clean fclean re