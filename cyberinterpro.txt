-- phpMyAdmin SQL Dump
-- version 5.1.1
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1:3306
-- Tempo de geração: 03-Nov-2022 às 14:25
-- Versão do servidor: 5.7.36
-- versão do PHP: 7.4.26
create database cyberinterpro;
use cyberinterpro;
SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Banco de dados: `cyberinterpro`
--

-- --------------------------------------------------------

--
-- Estrutura da tabela `tbcertificado`
--

DROP TABLE IF EXISTS `tbcertificado`;
CREATE TABLE IF NOT EXISTS `tbcertificado` (
  `certificadoid` int(11) NOT NULL AUTO_INCREMENT,
  `padrao` varchar(20) NOT NULL,
  `nome` varchar(100) NOT NULL,
  `cpf` char(9) NOT NULL,
  `senha` varchar(45) NOT NULL,
  `data_emissao` date DEFAULT NULL,
  `data_validade` date DEFAULT NULL,
  `certificadopdf` mediumblob,
  PRIMARY KEY (`certificadoid`,`cpf`)
) ENGINE=MyISAM AUTO_INCREMENT=19 DEFAULT CHARSET=latin1;

--
-- Extraindo dados da tabela `tbcertificado`
--

INSERT INTO `tbcertificado` (`certificadoid`, `padrao`, `nome`, `cpf`, `senha`, `data_emissao`, `data_validade`, `certificadopdf`) VALUES
(1, 'Juridico', 'asdasd', '', '0aa1ea9a5a04b78d4581dd6d17742627', '2022-11-03', '2025-11-03', NULL),
(17, 'Fisico', 'danilo', '2834238', 'Abc123', '2022-11-03', '2025-11-03', NULL),
(15, 'Fisico', 'danilo', '', '61bd60c60d9fb60cc8fc7767669d40a1', '2022-11-03', '2025-11-03', NULL),
(16, 'Fisico', 'danilo', '2834238', '61bd60c60d9fb60cc8fc7767669d40a1', '2022-11-03', '2025-11-03', NULL);

-- --------------------------------------------------------

--
-- Estrutura da tabela `tbusuario`
--

DROP TABLE IF EXISTS `tbusuario`;
CREATE TABLE IF NOT EXISTS `tbusuario` (
  `userid` int(11) NOT NULL AUTO_INCREMENT,
  `usuario` varchar(45) NOT NULL,
  `email` varchar(60) NOT NULL,
  `telefone` varchar(11) NOT NULL,
  `cpf` varchar(11) NOT NULL,
  `senha` varchar(45) NOT NULL,
  PRIMARY KEY (`userid`)
) ENGINE=MyISAM AUTO_INCREMENT=6 DEFAULT CHARSET=latin1;

--
-- Extraindo dados da tabela `tbusuario`
--

INSERT INTO `tbusuario` (`userid`, `usuario`, `email`, `telefone`, `cpf`, `senha`) VALUES
(1, 'uyhgytgty', 'hghghgh@gamil.com', '71487', '', '60131cf1fb645ce65a6c1f6f60b6e875'),
(2, 's ugfyukgtf', 'gdjusfyugtsd@gmail.com', '65.2982', '', '38054ae419be9e8290323bf41b89739a'),
(3, 'nic', 'nic@gmail.com', '6546735', '', 'gfeg$5jhjh'),
(4, 'danilo', 'danilo.danilo@gmail.com', '12312312', '', 'e99a18c428cb38d5f260853678922e03'),
(5, 'danilo', 'danilo@gmail.com', '1829', '2834238', '61bd60c60d9fb60cc8fc7767669d40a1');
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
