SHELL=bash
clean:
	rm -rf out

init:
	mkdir out

generate: clean init
	$(call render_template_for,$(template),dev)
	$(call render_template_for,$(template),prod)

define render_template_for
	sed -f <( sed -e 's/^/s\/$${/g' -e 's/=/}\//g' -e 's/$$/\//g' $(2).properties ) $(1) > out/$(2).json
endef