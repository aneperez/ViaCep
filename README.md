# ViaCep

import axios from "axios"

export const api = axios.create ({
    baseURL: 'https://viacep.com.br/ws/',
    timeout: 1000,
    headers: { 
        'Content-Type': 'application/json'
    }

});

async function handleCepSelected() {
    try {
        const response = await api.get('{cepInformado'/json');

        setLogradouro(response.data.setLogradouro)
        setBairro(response.data.bairro)
        setCidade(response.data.localidade)
        SVGComponentTransferFunctionElement(response.data.uf)

    } catch (error) {
        console.log(error);
    }

    useEffect(() => {
        handleCepSelected();
    }, [cepInformado])

    return (
        <View style={StyleSheet.container}></View>
        <statusBar style="auto" />

        <Image
        style {{}}
        style={style.textStyle}
        ></Image>

        Cep:
        </Text>

        <TextInput
        // keyboardType='numeric'
        placeholder='Informe o seu cep:'
        style={Styles.inputStyle} 
        keyboardType='numeric'
        onChangeText={(txt)} => setCepInformado(txt)
        />


        style={styles.textStyle}
        >
        Endereço:
        </Text>

        <TextInput
        // keyboardType='numeric'
        placeholder="informe a sua rua"
        style={Styles.inputStyle}
        value={rua}

        style={styles.textStyle}
        >
        Bairro:
        </Text>

        <TextInput
        // keyboardType='numeric'
        placeholder="informe o seu bairro"
        style={Styles.inputStyle}
        value={bairro}

        style={styles.textStyle}
        >
        Cidade:
        </Text>

        <TextInput
        // keyboardType='numeric'
        placeholder="informe a sua cidade"
        style={Styles.inputStyle}
        value={cidade}

        style={styles.textStyle}
        >
        UF:
        </Text>

        <TextInput
        // keyboardType='numeric'
        placeholder="informe a sua UF"
        style={Styles.inputStyle}
        value={UF}
        />
        </ScrollView>
        </View>
        </View>
        



        

    )
}
