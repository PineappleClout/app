# mobile-node
PoC Freenet mobile node

## How

By adding freenet.jar, wrapper.jar and other jars as dependences to gradle:


    dependencies {
        ...
        implementation files('libs/freenet.jar')
        ...   
    }   

Once added as libraries we can interact with Freenet:


    public class MainActivity extends AppCompatActivity {

        @Override
        protected void onCreate(Bundle savedInstanceState) {

            freenet.node.NodeStarter.main(args);

        }    

### Limitations

- Node won't be able to self update (in theory)

## Building

git clone https://github.com/freenet/fred
cd fred
./gradlew jar
 > copy build/libs/freenet.jar
