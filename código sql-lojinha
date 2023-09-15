--
-- Banco de dados: `loja`
--

-- --------------------------------------------------------

--
-- Estrutura para tabela `tbl_clientes`
--

CREATE TABLE `tbl_clientes` (
  `ID_Cliente` int(5) NOT NULL,
  `Nome_Cliente` varchar(50) NOT NULL,
  `CPF_Cliente` varchar(14) NOT NULL,
  `Data_Nasc` date NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

-- --------------------------------------------------------

--
-- Estrutura para tabela `tbl_produtos`
--

CREATE TABLE `tbl_produtos` (
  `ID_Produto` int(4) NOT NULL,
  `Nome_Prod` varchar(50) NOT NULL,
  `Categoria` varchar(50) NOT NULL,
  `Preco_Prod` decimal(8,0) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

-- --------------------------------------------------------

--
-- Estrutura para tabela `tbl_telefones`
--

CREATE TABLE `tbl_telefones` (
  `id_Fone` int(11) NOT NULL,
  `id_Cliente` int(11) NOT NULL,
  `Telefone` varchar(19) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

-- --------------------------------------------------------

--
-- Estrutura para tabela `tbl_vendas`
--

CREATE TABLE `tbl_vendas` (
  `ID_Venda` int(5) NOT NULL,
  `ID_Cliente` int(5) NOT NULL,
  `ID_Produto` int(6) NOT NULL,
  `Quantidade` int(3) NOT NULL,
  `Data_venda` date NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Índices de tabela `tbl_clientes`
--
ALTER TABLE `tbl_clientes`
  ADD PRIMARY KEY (`ID_Cliente`);

--
-- Índices de tabela `tbl_produtos`
--
ALTER TABLE `tbl_produtos`
  ADD PRIMARY KEY (`ID_Produto`);

--
-- Índices de tabela `tbl_telefones`
--
ALTER TABLE `tbl_telefones`
  ADD PRIMARY KEY (`id_Fone`),
  ADD KEY `id_Cliente` (`id_Cliente`);

--
-- Índices de tabela `tbl_vendas`
--
ALTER TABLE `tbl_vendas`
  ADD PRIMARY KEY (`ID_Venda`),
  ADD KEY `ID_Cliente` (`ID_Cliente`),
  ADD KEY `ID_Produto` (`ID_Produto`);

--
-- Restrições para tabelas `tbl_produtos`
--
ALTER TABLE `tbl_produtos`
  ADD CONSTRAINT `tbl_produtos_ibfk_1` FOREIGN KEY (`ID_Produto`) REFERENCES `tbl_vendas` (`ID_Produto`);

--
-- Restrições para tabelas `tbl_telefones`
--
ALTER TABLE `tbl_telefones`
  ADD CONSTRAINT `tbl_telefones_ibfk_1` FOREIGN KEY (`id_Cliente`) REFERENCES `tbl_clientes` (`ID_Cliente`);

--
-- Restrições para tabelas `tbl_vendas`
--
ALTER TABLE `tbl_vendas`
  ADD CONSTRAINT `tbl_vendas_ibfk_1` FOREIGN KEY (`ID_Cliente`) REFERENCES `tbl_clientes` (`ID_Cliente`);
COMMIT;
