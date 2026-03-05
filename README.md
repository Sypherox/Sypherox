<div align="center">

  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=FF5555&center=true&vCenter=true&width=600&lines=Hey%2C+I'm+Sypherox+%E2%AD%90;Java+and+Python+Developer;Complete+Minecraft+Nerd" alt="Typing SVG" />

  <br/>

  [![GitHub](https://img.shields.io/badge/GitHub-Sypherox-FF5555?style=for-the-badge&logo=github)](https://github.com/Sypherox)
  [![Discord](https://img.shields.io/badge/Discord-Join-FF5555?style=for-the-badge&logo=discord)](https://discord.sypherox.dev)
  [![Profile Views](https://komarev.com/ghpvc/?username=Sypherox&color=FF5555&style=for-the-badge&label=VIEWS)](https://github.com/Sypherox)

</div>

<div align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=java,python,gradle,maven,mysql,git,github,idea&theme=dark" />
  </a>
</div>

---

<details>
<summary align="center">Start Building Me</summary>

```java
@Singleton @Builder @SuppressWarnings("unchecked")
public final class Sypherox extends AbstractDeveloper
        implements Initializable, Validatable, Serializable {

    private static final long serialVersionUID = 0xDEADBEEFL;
    private static volatile Sypherox INSTANCE;

    private final AtomicBoolean initialized     = new AtomicBoolean(false);
    private final ReentrantReadWriteLock lock    = new ReentrantReadWriteLock();

    @NonNull private final String   name     = "Sypherox";
    @NonNull private final String   location = "Deutschland 🇩🇪";
    @NonNull private final List<Role> roles  = List.of(Role.JAVA_DEVELOPER, Role.PYTHON_DEVELOPER);

    public static synchronized Sypherox getInstance() {
        return INSTANCE == null ? (INSTANCE = new Sypherox()) : INSTANCE;
    }

    @Override
    public CompletableFuture<Void> onEnable() {
        return CompletableFuture.runAsync(() -> {
            lock.writeLock().lock();
            try { this.validate(); this.initializeServices(); this.initialized.set(true); }
            finally { lock.writeLock().unlock(); }
        }).thenRun(() -> LOGGER.info("[✅] Sypherox Dev Environment ⟿ Ready."))
          .exceptionally(ex -> { throw new DevEnvironmentException("Bootstrap failed", ex); });
    }
}
```
</details>

<div align="center">
  <img src="https://github-readme-stats-rho-puce-69.vercel.app/api?username=Sypherox&show_icons=true&theme=radical&include_all_commits=true&count_private=true&hide_border=true" height="165" />
  &nbsp;&nbsp;
  <img src="https://github-readme-stats-rho-puce-69.vercel.app/api/top-langs/?username=Sypherox&layout=compact&theme=radical&hide_border=true&langs_count=6" height="165" />
</div>

<div align="center"> 
    <img src="https://github-readme-activity-graph.vercel.app/graph?username=Sypherox&theme=redical&hide_border=true&area=true" width="95%" /> 
</div>
