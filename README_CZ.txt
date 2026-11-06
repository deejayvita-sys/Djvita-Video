DJVíťa Video – zdrojový Android projekt
========================================

Tato verze obsahuje základní lokální export MP4 pomocí AndroidX Media3 Transformer.

Co implementace umí:
- vybrat fotografii 1, fotografii 2 nebo vlastní video přes systémový výběr souborů;
- vybrat zvukovou skladbu;
- nastavit délku 10 / 20 / 30 / 60 sekund nebo délku podle ořezu skladby;
- oříznout začátek a konec hudby v sekundách;
- z fotografií vytvořit statické obrazové úseky (při dvou fotkách se střídají po sobě);
- u vlastního videa odstranit původní zvuk a použít vybranou skladbu;
- exportovat H.264/AAC do MP4 a uložit jej do Movies/DJVitaVideo, aby se zobrazil v Galerii.

Omezení, která tato verze záměrně nepředstírá:
- volba Realistický/Kreslený zatím nemění obraz;
- volba muž/žena/duet zatím není analýza hlasu;
- návrh scén podle textu je pouze rozpoznávání několika slov, ne AI;
- nejsou implementované generování nových scén, animace obličejů ani lip-sync;
- při vlastním videu je délka výsledku omezena délkou zdrojového videa;
- export závisí na kodecích a možnostech konkrétního telefonu a musí se otestovat na zařízení.

Sestavení APK:
1. Projekt vyžaduje Android SDK 35, JDK 17 a Gradle 8.9.
2. V kořeni projektu spusť: gradle --no-daemon assembleDebug
3. APK vznikne v app/build/outputs/apk/debug/app-debug.apk.

Pro sestavení bez počítače:
- lze projekt nahrát do vlastního GitHub repozitáře a spustit workflow
  .github/workflows/build-apk.yml přes Actions;
- GitHub účet a nahrání projektu jsou potřeba. Workflow pouze sestaví APK,
  samo o sobě aplikaci nenainstaluje do telefonu.

Žádná placená AI služba ani platba není součástí tohoto projektu.
