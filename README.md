# HIKKIxMORI

## Wymagania

- Unity Hub
- Unity Editor w wersji **6000.3.11f1** (dokładnie ta wersja)
- Git
- Git LFS

## Instalacja

1. W Unity Hub zainstaluj edytor w wersji 6000.3.11f1, jeśli go jeszcze nie masz ([https://unity.com/releases/editor/archive])



2. Zainstaluj Git LFS ([https://git-lfs.com]) i wykonaj jednorazowo na swoim komputerze:

   ```
   git lfs install
   ```

3. Sklonuj repozytorium do katalogu o krótkiej ścieżce, bez spacji i polskich znaków (np. `C:\Projekty`):

   ```
   git clone https://github.com/SKNlevelup/HIKKIxMORI.git
   cd HIKKIxMORI
   ```

## Otwarcie projektu

1. Uruchom Unity Hub.
2. Wybierz **Add > Add project from disk**.
3. Wskaż folder `HIKKIxMORI` (ten, w którym znajdują się `Assets`, `Packages` i `ProjectSettings`).
4. Otwórz projekt w wersji edytora 6000.3.11f1. Pierwsze uruchomienie może potrwać kilka minut, ponieważ Unity generuje folder `Library`.
5. Otwórz scenę startową z folderu `Assets/Scenes`.

## **Opcjonalnie:** Unity SmartMerge
Ułatwia scalanie scen i prefabów. Ustawienie jest lokalne i należy je wykonać w folderze repozytorium, w Windows PowerShell. Komenda zakłada domyślną lokalizację Unity Hub; przy innej instalacji należy zmienić ścieżkę do `UnityYAMLMerge.exe`.

```
git config merge.unityyamlmerge.name "Unity SmartMerge"
git config merge.unityyamlmerge.driver '\"C:\Program Files\Unity\Hub\Editor\6000.3.11f1\Editor\Data\Tools\UnityYAMLMerge.exe\" merge -p %O %B %A %A'
```

## Rozwiązywanie problemów

- **Grafiki lub modele nie wyświetlają się poprawnie:** pliki z Git LFS nie zostały pobrane. Wykonaj `git lfs install`, a następnie `git lfs pull`.
- **Unity zmienia `ProjectSettings` po otwarciu:** używana jest inna wersja edytora niż 6000.3.11f1.
- **Brakujące referencje:** sprawdź, czy pliki `.meta` znajdują się w repozytorium.
