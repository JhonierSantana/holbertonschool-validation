# Define variables
Publish=hugo

build: ## Build a new website
	$(Publish)

clean: ## Remove all files from folder dist
	rm -r dist/*

post: ## Create new post and usign the sed commando to modify the contents of a file
	$(Publish) new posts/$(POST_NAME).md
	sed -i 's/title: .*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md
# Overwrite the content of a text file without generating a new one (option -i)

help: ## Display the list of targets and their usage.
	cat Makefile | grep '##' | tr -d '##' | head -n -1

