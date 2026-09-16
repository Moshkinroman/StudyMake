# Makefile для example-3 (Kazino-Royal)
# Использует переменные для гибкости сборки

.PHONY: all debug release clean

# Флаги компиляции
RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall

# Имена исполняемых файлов
RELEASE_EXEC  = kazino
DEBUG_EXEC    = kazino-dbg

# Исходный файл (переменная для удобства изменения)
SOURCE        = Kazino-Royal.cpp

# Цель по умолчанию — собрать обе версии
all: debug release

# Debug-сборка
debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SOURCE)
	g++ $(DEBUG_FLAGS) $(SOURCE) -o $(DEBUG_EXEC)

# Release-сборка
release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SOURCE)
	g++ $(RELEASE_FLAGS) $(SOURCE) -o $(RELEASE_EXEC)

# Очистка артефактов сборки
clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)
