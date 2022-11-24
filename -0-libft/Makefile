# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: jomirand <jomirand@student.42porto.com>    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/11/08 12:16:42 by jomirand          #+#    #+#              #
#    Updated: 2022/11/16 14:32:47 by jomirand         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

SRC = ft_isalnum.c \
        ft_isalpha.c \
        ft_isdigit.c \
        ft_isprint.c \
        ft_isascii.c \
        ft_strlen.c \
        ft_memset.c \
        ft_bzero.c \
        ft_strlcpy.c \
        ft_strlcat.c \
        ft_toupper.c \
        ft_tolower.c \
        ft_strchr.c \
        ft_strrchr.c \
        ft_atoi.c \
        ft_strncmp.c \
        ft_memcpy.c \
        ft_memchr.c \
        ft_memcmp.c \
        ft_memmove.c \
        ft_strnstr.c \
        ft_calloc.c \
        ft_strdup.c \
        ft_substr.c \
        ft_strjoin.c \
        ft_strtrim.c \
        ft_split.c \
        ft_itoa.c \
        ft_strmapi.c \
        ft_striteri.c \
        ft_putchar_fd.c \
        ft_putstr_fd.c \
        ft_putendl_fd.c \
        ft_putnbr_fd.c \

OBJ = $(SRC:.c=.o)

BONUS = ft_lstadd_back.c \
        ft_lstadd_front.c \
        ft_lstclear.c \
        ft_lstdelone.c \
        ft_lstiter.c \
        ft_lstlast.c \
        ft_lstmap.c \
        ft_lstnew.c \
        ft_lstsize.c \

OBJ_BONUS = $(BONUS:.c=.o)

CC = cc
CFLAGS = -Wall -Wextra -Werror

NAME = libft.a

all: $(NAME)

$(NAME): $(OBJ)
	@ar rcs $(NAME) $(OBJ)
	@ranlib $(NAME)

clean:
	@rm -rf $(OBJ) $(OBJ_BONUS)

fclean: clean
	@rm -rf $(NAME)

re: fclean all

bonus: $(OBJ) $(OBJ_BONUS)
	@ar rcs $(NAME) $(OBJ) $(OBJ_BONUS)
	@ranlib $(NAME)

so:
	$(CC) -nostartfiles -fPIC $(CFLAGS) $(SRC) $(BONUS)
	gcc -nostartfiles -shared -o libft.so $(OBJ) $(OBJ_BONUS)
