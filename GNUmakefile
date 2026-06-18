PLACES_FILE   := $(abspath data/places.json)
TIMELINE_FILE := $(abspath timelines/Timeline.json)

BIN_DIR := $(abspath bin)
TMP_DIR := $(abspath tmp)

.PHONY: all clean export_places refresh_place_ids

all: clean refresh_place_ids export_places

clean:
	@rm -fr "$(TMP_DIR)"
	@mkdir -p "$(TMP_DIR)"

export_places:
	@uv run "$(BIN_DIR)/export_places" "$(TIMELINE_FILE)" "$(TMP_DIR)/places.json" "$(TMP_DIR)/layers"

refresh_place_ids:
	@uv run "$(BIN_DIR)/refresh_place_ids" "$(TIMELINE_FILE)" "$(PLACES_FILE)" > "$(TMP_DIR)/places.json"
